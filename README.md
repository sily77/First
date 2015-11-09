# First

import random
class game(object):
	def fuwei(self):
		self.x=0
		self.win=0

	def hud(self):
		
		t = 0
		n = 0
		while(t < 3):
			a=random.randint(1,6)
			#print(a,"作弊参数")
			choice=input("choice big or small:")
			if(choice =="big" or choice == "small"):
				if(choice == "big" and a > 3):
					print("You are right!")
					n += 1
				elif(choice == "small" and a <4):
					print("You are right!")
					n += 1
				else:
					print("You are wrong!")
				t +=1
		if(n >= 2):
			print("You are win!!!!!!!!!!!!!")
			self.win += 1
		else:
			print("You are lost!No ploblem,you can try again!")
		self.x += 1
	
	def xuan(self):
		while(True):
			choice = input("Are you try again: y/n")
			if(choice == "y" or choice == "n"):
				if(choice == "y"):
					self.hud()
				if(choice == "n"):
					print("you play %d and win %d" % (self.x,self.win))
					return
def main():
	a = game()
	a.fuwei()
	a.hud()
	a.xuan()

main()	
