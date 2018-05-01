import gym
import universe 
import random

#re inforcement learning step
def determine_trn(turn,observation_n, j , total_sum, prev_total_sum, reward_n):
	#for every 15 iterations , sum the total observations, and take the average
	#if lower than 0, change the direction

	#if we go 15 iteitaion and more get a rewad each step, we're doing somthing right
	#thats when we turn

	if(j == 15):

		if(total_sum/j) == 0:
			turn = True
		else:
			turn = False

			#reset variables
			total_sum = 0
			j = 0
			prev_total_sum = total_sum
			total_sum = 0

		else:
			turn = false
		if(observation_n != None):
			#increment counter and reward sum 
			j+= 1
			total_sum += reward_n
		return(turn, j , total_sum, prev_total_sum)





def main():
#init enironment
	env =gym.make('flashgames.CosterRacer-v0')
	#initalizing the env 
	#client is the agent
	#remote is the environment (local)
	observation_n = env.reset()
	#init variables 
	#no of game iterations
	n = 0
	j = 0
	#sum of observations 
	total_sum = 0
	prev_total_sum = 0
	turn = False

	#define our turns or keyboard actions 
	left = [('KeyEvent', 'ArrowUp',True) , ('KeyEvent', 'ArrowLeft', True), ('KeyEvent','ArrowRight', False)]
	right = [('KeyEvent', 'ArrowUp',True) , ('KeyEvent', 'ArrowLeft', False), ('KeyEvent','ArrowRight', True)]
	Forward  = [('KeyEvent', 'ArrowUp',True) , ('KeyEvent', 'ArrowLeft', False), ('KeyEvent','ArrowRight', False)]

	#main logic
	while True:
		#increment a counter for number of iterations
		n+=1

		#if at least one iteration is made , check if a turn is needed
		if(n>1):

			if(observation_n[0] != None):
				#store the revard in the previous score
				prev_score = r eward_n[0]


				if(turn):
			  		#pic a random event
			  		#where to turn
			  		event = random.choice([left,right])
			  		#perform an action 
			  		action_n = [event for ob in observation_n]
			  		turn = False
			  		#bcs we have alredy turned

			  	elif(~turn):
			  		#if no turn is neede , go straight
			  		action_n = [Forward for ob in observation]


			  	#if there is an observation , game has started 
			  		if (observation_n[0] != None):
			  			turn, j , total_sum, prev_total_sum = determine_turn(turn, observation_n[0], j, total_sum, reward_n[0]

			  			#save new variable for ech iteration
			  			observation_n, reward_n done_n, info = env.step(ation_n)


if_name_ = '_main_':
	main()			  			

