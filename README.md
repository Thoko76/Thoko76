from flask import Flask


app = Flask(__name__)

@app.route('/') #decorator
def index():
   return "flask works!"


# routing: 사용자의 접속 경로를 지정

# 외부 api 정보 가져오기
  
@app.route('/posts')
 def show_posts():
   return "This is blog posts"

# /todos -> "This is todos"
   
if __name__=='__main__':
  app.run(host='0.0.0.0', port=5000, debug=True)
  #프로젝트 첫 시작시 pip install flask 실행해야함.
# shell에서 app 시작: $ python main.py
