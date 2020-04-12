#coding:gbk
"""
第一个小项目：Rock-paper-scissors-lizard-Spock
程序作者:孙奥楠
"""
import random

# 0 - 石头
# 1 - 史波克
# 2 - 纸
# 3 - 蜥蜴
# 4 - 剪刀
computer_guess=random.randint(0,4)            #计算机产生随机数
num=computer_guess
def name_to_num(name):
	if name=="石头":
		return 0
	elif name=="史波克":
		return 1
	elif name=="纸":
		return 2
	elif name=="蜥蜴":
		return 3
	elif name=="剪刀":
		return 4
	#else:
		#print('Please input name among:"石头", "史波克", "纸", "蜥蜴", or "剪刀".')
	

def num_to_name(num):
	if num in range(0,5):
		if num==0:
			return '石头'
		elif num==1:
			return '史波克'
		elif num==2:
			return '纸'
		elif num==3:
			return '蜥蜴'
		elif num==4:
			return '剪刀'
	else:
		print("Please input number in the range 0 to 4.")
			 
			 		
def rpsls(player_choice):
		print()
		print("您的选择",player_choice)
		player_num = name_to_num(player_choice)
		comp_num = random.randrange(0,5)
		comp_choice = num_to_name(comp_num)
		print("计算机的选择",comp_choice)
		if player_num - comp_num in range(-4,-2) or range(1,3):
			print('您赢了!')
		elif player_num - comp_num in range(-2,0) or range(3,5):
			print('计算机赢了!')
		elif player_num - comp_num == 0:
			print("平局")
		else:
			print("错误了")

	

print("欢迎使用RPSLS游戏")
print("----------------")
print("请输入您的选择:")
choice_name=str(input())
aaa=rpsls(choice_name)
