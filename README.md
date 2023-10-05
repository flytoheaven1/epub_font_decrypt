# epub_font_decrypt
* 기본 사용법
1. font_decrypt.py totxt -p [file.epub] -o [file.txt]
2. font_decrypt.py cmap -f [원본폰트.ttf] -o [original_font_cmap.json]
3. font_decrypt.py backup -f [원본폰트.ttf] -o [original_font_backup.json]
4. font_decrypt.py backup -f [epub폰트.ttf] -o [epub_font_backup.json]
5. font_decrypt.py dump -std [original_font_backup.json] -cmp [epub_font_backup.json] -c [original_font_cmap.json] -o [dump.json]
6. font_decrypt.py decrypt -p [file.txt] -d [dump.json] -o [decrypt.txt]

* 누락된 문자가 있을 경우
1. 터미널에서 누락된 문자열에 대응하는 10진수 값 확인
2. dump.json 수정 - {"10진수값": "실제문자", ...}