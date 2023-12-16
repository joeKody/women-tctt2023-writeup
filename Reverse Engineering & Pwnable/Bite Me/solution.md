# Bite me
- decompile ไฟล์ pyc ออกมา (https://www.toolnb.com/tools-lang-en/pyc.html)
- bruteforce เอา
```py
import hashlib

def test(current):
	text = 'oh_my_got_snake_bite_me!!' + str(current)
	md5 = hashlib.md5(text.encode()).hexdigest()
	flag = ''
	for i in range(len(md5)):
	    if i % 2 == 0:
        	flag += hex(ord(md5[i]) ^ ord(md5[(i + 1)]))[(-1)]
	    else:
	        flag += hex((eval('0x' + md5[i]) + 13) % 16)[(-1)]

	flag = 'WCTF23{' + flag + '}'
	check1 = hashlib.md5(flag.encode()).hexdigest()
	if check1 == '4491e4dd73fc581560bc430fd55fce15':
	    print(flag)
	    print(current)

for i in range(1, 1000000):
	test(i)
```