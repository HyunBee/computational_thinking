#20180268김현비

#yes24사이트에서 베스트셀러목록 추출

import urllib.request

r = urllib.request.urlopen('http://www.yes24.com/24/category/bestseller').read()


#여기서 유니코드 오류때문에 한국어 출력이 안됨. 12일에 상담한 멘토님께서 다른 멘토님께 여쭤보라고 하심.

script=str(r.text)

script= script.replace('<', ' ') 
script= script.replace('<p id="', ' ') 
script= script.replace(',',' ') 
script= script.replace('.',' ') 
script= script.replace("'",' ') 
script= script.replace(">",' ') 
script= script.replace('/',' ') 
script= script.replace('"',' ')
script= script.replace("=",' ') 
script=script.replace(' p ', ' ')




#추출한 목록에서 작가, 출판사 추출해서 베스트셀러 목록과 연결짓는 dic 생성


input("관심있는 책은?")

#관심있다고 입력한 책에 따라 출판사, 작가 정보 제공
