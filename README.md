# epub_font_decrypt
* 기본 사용법
1. dump.py -txt [test.xhtml] -o [test.txt]
2. dump.py -coords [original_font.ttf] -o [dump_coords.json] - 재사용 가능
3. dump.py -coords [Obfuscated_font.ttf] -o [Obfuscated_dump_coords.json]
4. dump.py -cmap [original_font.ttf] -o [dump_cmap.json] - 재사용 가능
5. dump.py -mapping [dump_coords.json] [Obfuscated_dump_coords.json] [dump_cmap.json] -o [dump_mapping.json]
6. dump.py -decrypt [test.txt] [dump_mapping.json] -o [decrypt_test.txt]

* 누락된 문자가 있을 경우
1. 커맨드에서 누락된 문자열에 대응하는 10진수 값 확인
2. dump_mapping.json 수정 - {"10진수값": "실제문자", ...}