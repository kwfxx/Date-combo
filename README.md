from concurrent.futures import ThreadPoolExecutor
from asmix import Instagram
from requests import get
import requests
import random
import string
import json
import os
import ethan

executor = ThreadPoolExecutor(max_workers=30)
Z = '\033[1;31m' #احمر
R = '\033[1;31m' #احمر
X = '\033[1;33m' #اصفر
F = '\033[2;32m' #اخضر
C = "\033[1;97m" #ابيض
B = '\033[2;36m'#سمائي
Y = '\033[1;34m' #ازرق فاتح.
E = '\033[1;31m'
B = '\033[2;36m'
G = '\033[1;32m'
S = '\033[1;33m'

ab=0

def kl():
 global ar ,ab
 try:
  LsD = ''.join(random.choices(string.ascii_letters + string.digits, k=4))
  
  UseriD = str(random.randrange(10000,uid))
  
  variables = json.dumps({"id": UseriD, "render_surface": "PROFILE"})
  data = {"lsd": LsD, "variables": variables, "doc_id": "25618261841150840"}
  
  response = requests.post("https://www.instagram.com/api/graphql", headers={"X-FB-LSD": LsD}, data=data)
  user= response.json()['data']['user']['username']


  pasw= user
  
  
  print(f'''
  {ab} / {user} / {pasw}
  ''')
  ab+=1
  with open('combo.txt', 'a') as f:
  	f.write(f'{user}:{pasw}'+'\n')
  
  
 except:
  ar+=1

  
print('''
1 -  2011
2 - 2012
3 - 2013
4 - 2014
5 - 2015
6 - 2016-2017
''')
num = int(input('choice<=> : '))


if num == 1:
    uid = 18957403
    iud = 10000
elif num == 2:
    uid = 287924624
    iud = 183140
elif num == 3:
    uid = 461365132
    iud = 180165130
elif num == 4:
    iud = 361365132
    uid = 1682665388
elif num == 5:
    iud = 1682665388
    uid = 3382665388
elif num == 6:
    iud = 2682665388
    uid = 8682665388
else:
    exit() 
for _ in range(10000000):
 executor.submit(kl)
