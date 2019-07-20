# typing-game-in-Python
import random
import time

sentences=["조명에는 여자의 안색을 망치는 음영이 있다."
           ,"There are certain shades of limelight that can wreck a girl's complexion."
          ,"내 신체에 감사하는 것이 자신을 더 사랑하는 열쇠임을 비로소 깨달았다."
           ,"I finally realized that being grateful to my body was key to giving more love to myself."
          ,"훌륭한 사람은 실패를 통해 지혜에 도달하기 때문에 훌륭한 것이다."
          ,"Good people are good because they've come to wisdom through failure."
          ,"나이가 들수록 해보지 않았던 것에 대해서만 후회한다는 것을 발견하게 될 것이다."
          ,"As you grow older, you'll find the only things you regret are the things you didn't do."
          ,"행복을 탐욕스럽게 좇지 말며, 두려워하지 마라."
          ,"Seek not happiness too greedily, and be not fearful of happiness."
          ,"나를 파괴시키지 못하는 것은 무엇이든지 나를 강하게 만들 뿐이다."
          ,"Whatever does not destroy me makes me stronger."
          ,"죽음은 삶보다 보편적이다. 모든 사람은 죽기 마련이지만 모든 이가 사는 것은 아니다."
          ,"Death is more universal than life; everyone dies but not everyone lives."
          ,"미래를 창조하기에 꿈만큼 좋은 것은 없다. 오늘의 유토피아가 내일 현실이 될 수 있다."
          ,"There is nothing like dream to create the future. Utopia today, flesh and blood tomorrow."]
n=1
print("\n[system]타자게임에 오신 것을 환영합니다.\n")
while True:
    menu=input("\n[system]\n0번_게임방법\t1번_게임시작\n2번_게임 나가기\n")
    if menu=='0':
        print("\n==========\n화면에 보이는 한글/영어 문장을 오타없이 바르게 입력하세요.\n맞은 문장만큼 포인트를 얻으며, 총 플레이 시간이 기록됩니다.\n==========\n")
    elif menu =='1':
        n=1
        print("\n[system]준비되면 enter키를 누르세요.\n")
        input()
        start=time.time()
        que=random.choice(sentences)
        while n<=5:
            print("\n[문제",n,"]\n")
            print(que)
            x=input()
            if que==x:
                print("\n통과!\n")
                n+=1
                que=random.choice(sentences)
            else:
                print("\n오타! 다시 도전하세요!\n")
        end=time.time()
        et=end-start
        et=format(et,'.2f')
        print("\n======\n타자시간:",et,"초","\n======\n")
    elif menu=='2':
        print("\n게임을 종료합니다.\n플레이해주셔서 감사합니다.\n")
        break
        
        
