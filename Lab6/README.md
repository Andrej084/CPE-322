Andrejs-MBP:~ andrejthekoolaidman$ cd ~/iot/lesson6
Andrejs-MBP:lesson6 andrejthekoolaidman$ npm -v
9.7.2
Andrejs-MBP:lesson6 andrejthekoolaidman$ node -v
v18.16.1
Andrejs-MBP:lesson6 andrejthekoolaidman$ node -h
Usage: node [options] [V8 options] [script.js] [arguments]
       node inspect [script.js | port]
       …
Andrejs-MBP:lesson6 andrejthekoolaidman$


Andrejs-MBP:lesson6 andrejthekoolaidman$ node hello.js
Server running at http://127.0.0.1:8080/
response end call done
request end event fired
response end call done
request end event fired
^C
Andrejs-MBP:lesson6 andrejthekoolaidman$


Andrejs-MBP:lesson6 andrejthekoolaidman$ node http.js
0
1
2
3
4
5
6
^C
Andrejs-MBP:lesson6 andrejthekoolaidman$


Andrejs-MBP:lesson6 andrejthekoolaidman$ pip install -U pystache
Collecting pystache
  Using cached pystache-0.6.5-py3-none-any.whl (81 kB)
Installing collected packages: pystache
Successfully installed pystache-0.6.5

[notice] A new release of pip is available: 23.2.1 -> 23.3.1
[notice] To update, run: python3 -m pip install --upgrade pip
Andrejs-MBP:lesson6 andrejthekoolaidman$


Andrejs-MBP:lesson6 andrejthekoolaidman$ cat say_hello.mustache
Hello, {{to}}!!
Andrejs-MBP:lesson6 andrejthekoolaidman$ cat say_hello.py
# https://github.com/defunkt/pystache
import pystache
print(pystache.render('Hi {{person}}!', {'person': 'Alexa'}))

class SayHello(object):
    def to(self):
        return "World"
hello = SayHello()

renderer = pystache.Renderer()
print(renderer.render(hello))

parsed = pystache.parse('Hey {{#who}}{{.}}{{/who}}')
print(parsed)
print(renderer.render(parsed, {'who': 'Google'}))
print(renderer.render(parsed, {'who': 'Siri'}))
Andrejs-MBP:lesson6 andrejthekoolaidman$ python3 say_hello.py
Hi Alexa!
Hello, World!
['Hey ', _SectionNode(key='who', index_begin=12, index_end=18, parsed=[_EscapeNode(key='.', '')])]
Hey Google!
Hey Siri!
Andrejs-MBP:lesson6 andrejthekoolaidman$
