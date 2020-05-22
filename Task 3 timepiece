from flask import Flask, render_template
import random
import time

app = Flask(_name_)

@app.route("/")
def index():
  return render_template("index.html")
 
@app.route("/hours")
def hours():
  now = time.gmtime()
  hours = now.tm_hour
  piece = ("white")
  
  if hours > 12:
      piece = ("red")
      hours = hours - 12
  draughts_pieces = [piece]*hours
  return render_template("hours.html", draughts_pieces = draughts_pieces)

@app.route("/minutes")
def minutes():
  now = time.gmtime
  mins = now.tm_min
  piece = ("white")
  
  if (1 <= mins <= 30):
    piece = ("red")
  if (31 <= mins <= 59):
    mins = 60 - mins
    
  draughts_pieces = [piece] *mins
  return render_template("minutes.html", draughts_pieces = draughts_pieces)
  
@app.route("/seconds")
def seconds():
  now = time.gmtime()
  secs = now.tm_sec
  draughts_pieces = []
  
  for x in range(0, secs):
      piece = random.choice(["red", "white"])
      draughts_pieces.append(piece)
      
  draughts_pieces = [piece]*secs
  return render_template("seconds.html", draughts_pieces = draughts_pieces)
  
  if _name_ == "_main_":
  app.run()
