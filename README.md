# epub_font_decrypt
* 기본 사용법
1. dump.py -t [test.xhtml] -o [test.txt]
2. dump.py -b [원본폰트.ttf] -o [original.json]
3. dump.py -b [epub폰트.ttf] -o [encrypt.json]
4. dump.py -c [원본폰트.ttf] -o [cmap.json]
5. dump.py -m [original.json] [encrypt.json] [cmap.json] -o [mapping.json]
6. dump.py -d [test.txt] [mapping.json] -o [decrypt_test.txt]

* 누락된 문자가 있을 경우
1. 터미널에서 누락된 문자열에 대응하는 10진수 값 확인
2. dump_mapping.json 수정 - {"10진수값": "실제문자", ...}