# rockpaperscissor-game

import random
opponent_history = []
def player(prev_play, opponent_history=opponent_history):
  if prev_play:
    opponent_history.append(prev_play)
    guess = "R"
    if len(opponent_history) >= 5:
      recent_moves = opponent_history[-5:]
      most_common = max(set(recent_moves), key=recent_moves.count)
      if most_common == 'R':
        guess = 'P'
      elif most_common == 'P':
        guess = 'S'
      else:
        guess = 'R'
  else:
    guess = random.choice(['R', 'P', 'S'])
  return guess

import subprocess
import sys
import random

# Install matplotlib if not already installed
subprocess.check_call([sys.executable, "-m", "pip", "install", "matplotlib"])

opponent_history = []
def player(prev_play, opponent_history=opponent_history):
  if prev_play:
    opponent_history.append(prev_play)
    guess = "R"
    if len(opponent_history) >= 5:
      recent_moves = opponent_history[-5:]
      most_common = max(set(recent_moves), key=recent_moves.count)
      if most_common == 'R':
        guess = 'P'
      elif most_common == 'P':
        guess = 'S'
      else:
        guess = 'R'
  else:
    guess = random.choice(['R', 'P', 'S'])
  return guess
