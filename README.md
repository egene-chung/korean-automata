# korean-automata : 한글 오토마타 만들기
<h3>1. 한글 도메인 지식</h3>

* 한글은 음절단위로 음절은 초성-중성-종성으로 이루어 진다.
* 한글은 단어와 단어 사이는 빈칸을 하나씩 넣어야 한다.
* 음절의 경우에는 초성-중성, 초성-중성-종성은 가능하지만 초성이 없는 경우는 불가능하고, 중성도 꼭 필요하다.
* 이러한 단어 단위는 연속적으로 이어지게 되는 오토마타를 이루게 된다.

<br><h3>2. 한글의 자음은 17개, 모음은 11개로 구성되어 있습니다. 초성, 중성, 종성에서는 다음의 문자가 사용됩니다.</h3>

* 한글 초성 : 19개 (ㄱ ㄲ ㄴ ㄷ ㄸ ㄹ ㅁ ㅂ ㅃ ㅅ ㅆ ㅇ ㅈ ㅉ ㅊ ㅋ ㅌ ㅍ ㅎ)
* 한글 중성 : 21개 (ㅏ ㅐ ㅑ ㅒ ㅓ ㅔ ㅕ ㅖ ㅗ ㅘ ㅙ ㅚ ㅛ ㅜ ㅝ ㅞ ㅟ ㅠ ㅡ ㅢ ㅣ)
* 한글 종성 : 28개 ((없음) ㄱ ㄲ ㄳ ㄴ ㄵ ㄶ ㄷ ㄹ ㄺ ㄻ ㄼ ㄽ ㄾ ㄿ ㅀ ㅁ ㅂ ㅄ ㅅ ㅆ ㅇ ㅈ ㅊ ㅋ ㅌ ㅍ ㅎ)


<br><h3>3. 다음 가능 문자열과 불가능 문자열을 한글 오토마타로 표현하고 입력하면 가능한지 불가능한지를 알려주어야 함.</h3>
* 가능 문자열: 가, 나, 다, 간, 난, 단, 갊, 낢, 닮, 집에 간다,…..
* 불가능 문자열: ㄱ, ㄴ, ㄷ, ㅓ, ㅏ, ㅙ, ㅞ, 갈ㄷ, 닭ㄱ, 구ㅐ, 괳ㄴ, ㅏㅣ,집ㅂ에다 …….
* 문장단위도 가능: 나는 이화여자대학교 학생이다(o), 나는 이화여자대ㅎ학교 ㅎㅎ학생(x)


<br><h3>4. 특수문자, 숫자, 빈칸이 input_string에 들어올 경우: epsilon으로 간주</h3>
<img width="1346" alt="image" src="https://github.com/egene-chung/korean-automata/assets/123860864/16070830-b963-4834-b3ac-d10fd6904d30">

<br>

---
