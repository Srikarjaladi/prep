# prep
MERGING MEETING TIMES:

      Your company built an in-house calendar tool called HiCal. You want to add a feature to see the times in a day when everyone is available.

      To do this, you’ll need to know when any team is having a meeting. In HiCal, a meeting is stored as a tuple ↴ of integers (start_time, end_time). These integers represent the number of 30-minute blocks past 9:00am.

      For example:

      (2, 3)  # Meeting from 10:00 – 10:30 am
      (6, 9)  # Meeting from 12:00 – 1:30 pm

      Write a function merge_ranges() that takes a list of multiple meeting time ranges and returns a list of condensed ranges.

      For example, given:

        [(0, 1), (3, 5), (4, 8), (10, 12), (9, 10)]

      your function would return:

        [(0, 1), (3, 8), (9, 12)]

      Do not assume the meetings are in order. The meeting times are coming from multiple teams.

      Write a solution that's efficient even when we can't put a nice upper bound on the numbers representing our time ranges. Here we've simplified our times down to the number         of 30-minute slots past 9:00 am. But we want the function to work even for very large numbers, like Unix timestamps. In any case, the spirit of the challenge is to m  erge         meetings where start_time and end_time don't have an upper bound. 

REVERSE STRING IN PLACE:
      
      Write a function that takes a list of characters and reverses the letters in place
      ANS:We swap the first and last characters, then the second and second-to-last characters, and so on until we reach the middle. 

REVERSE WORDS:
      
       You're working on a secret team solving coded transmissions.

      Your team is scrambling to decipher a recent message, worried it's a plot to break into a major European National Cake Vault. The message has been mostly deciphered, but         all the words are backward! Your colleagues have handed off the last step to you.

      Write a function reverse_words() that takes a message as a list of characters and reverses the order of the words in place
      EX: 'CAKE POUND STEAL' -> 'STEAL POUND CAKE'

MERGE SORTED ARRAYS:

       In order to win the prize for most cookies sold, my friend Alice and I are going to merge our Girl Scout Cookies orders and enter as one unit.
       Each order is represented by an "order id" (an integer).
       We have our lists of orders sorted numerically already, in lists. Write a function to merge our lists of orders into one sorted list. 
       EX: my_list     = [3, 4, 6, 10, 11, 15] , alices_list = [1, 5, 8, 12, 14, 19]
       # Prints [1, 3, 4, 5, 6, 8, 10, 11, 12, 14, 15, 19]
       print(merge_lists(my_list, alices_list))
       We can do this in O(n) time and space. If we are using a built in function it will take O(nlogn).

SUPER BALANCED TREE:

        A tree is "superbalanced" if the difference between the depths of any two leaf nodes ↴ is no greater than one. 
        We do a depth-first walk ↴ through our tree, keeping track of the depth as we go. When we find a leaf, we add its depth to a list of depths if we haven't seen that depth             already.
        Each time we hit a leaf with a new depth, there are two ways that our tree might now be unbalanced:
        There are more than 2 different leaf depths
        There are exactly 2 leaf depths and they are more than 1 apart.
        Why are we doing a depth-first walk and not a breadth-first ↴ one? You could make a case for either. We chose depth-first because it reaches leaves faster, which allows us to         short-circuit earlier in some cases. 
        Complexity: O(n) time and O(n) space
         For time, the worst case is the tree is balanced and we have to iterate over all nnn nodes to make sure.

          For the space cost, we have two data structures to watch: depths and nodes.

          depths will never hold more than three elements, so we can write that off as O(1).

          Because we’re doing a depth first search, nodes will hold at most ddd nodes where ddd is the depth of the tree (the number of levels in the tree from the root node down               to the lowest node). So we could say our space cost is O(d).

          But we can also relate ddd to nnn. In a balanced tree, ddd is O(log⁡2(n)). And the more unbalanced the tree gets, the closer ddd gets to nnn.

          In the worst case, the tree is a straight line of right children from the root where every node in that line also has a left child. The traversal will walk down the line             of right children, adding a new left child to nodes at each step. When the traversal hits the rightmost node, nodes will hold half of the nnn total nodes in the tree. Half           n is O(n), so our worst case space cost is O(n). 
