# #100DaysOfCode Log - Round 1 - [Y. Budhachandra Singh]

The log of my #100DaysOfCode challenge. Started on [September 23, Sunday, 2018].

## Log

### R1D1 
Started a Weather App. Worked on the draft layout of the app, struggled with OpenWeather API http://www.example.com

### R1D2
Dont really know what to do yet....

### R1D7
code for today:
from os import system, name
from random import *
print("Movies & Series __quotes__")
print("--------------------------")
##use choice(list_name) -- to select random element from list

##algorithms
# run in while loop
# select qoutes from movies or Series
# add or delete qotes
# print qoutes

log = True

movie_quotes = ["Keep your friends close, but your enemies closer. --THE GODFATHER PART II", "where we're going, we dont need roads -- Back to the future", " The greatest trick the Devil ever pulled was convincing the world he didn’t exist -- The Usual Suspects"]
series_quotes = ["one who wears the crown, bears the crown  -- The Heirs", "we're just acting like we dont know -- Boys Over Flowers", "If you only face forward, there is something you will miss seeing. -- Vash the Stampede"]

```python
def clear():
  #for windows
  if name == 'nt':
    _ = system('cls')
  #for linnux, osX
  else:
    _ = system('clear')

print("""
  MENU
    m = movie quotes
    s = series quotes
    m+ = add movie quote
    m- = remove movie quote
    s+ = add series quote
    s- = remove series quote
    p = print quotes
    f = press f to quit
    c = clear
 """)

while log == True:
  promt = input("Enter a command from the menu \n>_ ").lower()
  if promt == 'm':
    print(choice(movie_quotes))
  elif promt == 's':
    print(choice(series_quotes))

  elif promt == 'm+':
    newMqu = input("enter your movie quote : ")
    movie_quotes.append(newMqu)
  elif promt == 'm-':
    olMqu = input("remove your movie quote : ")
    if olMqu in movie_quotes:
      movie_quotes.remove(olMqu)
    else:
      print("quote not in list")
  elif promt == 's+':
    newSqu = input("enter your series quote : ")
    series_quotes.append(newSqu)
  elif promt == 's-':
    olSqu = input("remove your series quote : ")
    if olSqu in series_quotes:
      movie_quotes.remove(olSqu)
    else:
      print("quote not in list")
  
  elif promt == 'p':
    print("MOVIE QUOTES :",movie_quotes)
    print("\n\nSERIES QUOTES:",series_quotes)
  elif promt == 'f':
    log = False
  elif promt == 'c':
    clear()
  else:
    print("choose a valid response")
```

