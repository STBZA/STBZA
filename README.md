import random

def guess_number():
    # 生成一个1到100之间的随机数
    secret_number = random.randint(1, 100)
    
    print("欢迎来到猜数字游戏！")
    print("我已经选好了一个1到100之间的数字，请你来猜。")
    
    attempts = 0
    while True:
        guess = int(input("你猜是多少？（输入你的猜测数字）："))
        attempts += 1
        
        if guess < secret_number:
            print("太小了！再试一次。")
        elif guess > secret_number:
            print("太大了！再试一次。")
        else:
            print(f"恭喜你，你猜对了！答案是{secret_number}。")
            print(f"你一共猜了{attempts}次。")
            break

if __name__ == "__main__":
    guess_number()
