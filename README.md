# Rock_Paper_Scissors
Rock paper scissors is a hand game originating in China, usually played between two people, in which each player simultaneously forms one of three shapes with an outstretched hand.

      import random
      import sys
      wins = 0
      losses = 0
      ties = 0
      while True:
          print('%s wins, %s losses, %s ties' % (wins, losses, ties))
          while True:
              print('Enter your move: (r)ock , (p)aper , (s)cissors or (q)uit')
              player_move = input()
              if player_move == 'q':
                  print('Thank you for playing :D')
                  sys.exit()
              elif player_move =='r' or player_move =='p' or player_move =='s':
                  break
              print('Type one of the r,p,s or q.')
          if player_move == 'r':
              print('ROCK vs. ...')
          elif player_move == 'p':
              print('PAPER vs. ...')
          elif player_move == 's':
              print('SCISSORS vs. ...')
          random_number = random.randint(1,3)
          if random_number == 1:
              computer_move = 'r'
              print('ROCK')
          elif random_number == 2:
              computer_move = 'p'
              print('PAPER')
          elif random_number == 3:
              computer_move = 's'
              print('SCISSORS')
          if player_move == computer_move:
              print('Ties')
              ties = ties + 1
          elif player_move == 'r' and computer_move == 'p':
              print('You LOST :(')
              losses = losses + 1
          elif player_move == 'r' and computer_move == 's':
              print('You WON :)')
              wins = wins + 1
          elif player_move == 'p' and computer_move == 'r':
              print('You WON :)')
              wins = wins + 1
          elif player_move == 'p' and computer_move == 's':
              print('You LOST :(')
              losses = losses + 1
          elif player_move == 's' and computer_move == 'r':
              print('You LOST :(')
              losses = losses + 1
          elif player_move == 's' and computer_move == 'p':
              print('You WON :)')
              wins = wins + 1

