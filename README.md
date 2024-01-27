# python_hagman
name=input("what is your name?")
print("hello,"+name,"time to display Hangman!")
import time
time.sleep(0.5)
print("Start Guessing")
word=("apple")
guesses=' '
turns=10
while turns>0:
  failed=0
  for char in word:
   if char in guesses:
    print(char,end=" ")
  else:
    print("-",end=" ")
    failed+=1
  if failed==0:
    print("you won")
    break

  guess=input("guess a character: ")
  guesses+=guess

  if guess not in word:
    turns-=1
    print("wrong")
    print("you have",+turns,'more guesses')
  if turns==0:
    print("you lose")
