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
