# Grid
- 1.Life Before Grid
    * flexbox는 옆으로 두거나 가운데로 옮기거나 나누기등은 쉽지만 격자모양(grid)는 만들기 어려움
    *  grid를 사용하면 보다 쉽게 모양을 만들 수 있음
- 2.CSS Grid Basic Concepts
    * Grid로 부모(father)에서 일어남
    * grid-template-columns 를 이용하여 column값을 줄 수 있음(적는 숫자 순서대로 box순서별로 크기적용)
    * row크기를 주지 않으면 child의 font크기에 따라 row값 설정
    * column(row)-gap을 이용하여 box간 간격줄 수 있음(gap만 사용하면 행렬 간격 한번에 가능)
- 3.Grid Temlplet Areas
    * 행과열에 같은 크기의 값을 반복적으로 할당하여 줄때 repeat함수를 사용=>repeat(반복횟수,크기)
    * auto함수는 전체를 사용 => auto (크기)
    * 부모의 grid-template-area와 자식의 grid-area에 있는 이름이 같아야함
    * grid-templet-area를 사용하면 원하는 위치에 box를 배치가능(빈공간은 .)
- 4.Rows and Column
    * 부모영역에서 영역을 지정하지 않고 자식영역에서 grid-column(row)-start(end)를 주면 각 자식영역 별로 범위 지정 가능=>숫자는 선의 순서를 기준으로
- 5.Shortcuts
    * grid-column(row)에서 start,end를 따로 지정하지 않고 (start)/(end)로 한번에 표기 가능
    * 맨 끝은 -1로 표기가능 => 맨 끝부터 -1,-2....
    * 시작과 끝을 적지 않아도 span (cell개수)로 표기가능 => 숫자만큼 공간을 차지
- 6.Line Namimg
    * 부모 gird영역에 [라임 이름]을 표기, 자식 영역에서 라인숫자 대신 이름사용
- 7.Grid Template
    * fraction : 사용공간을 뜻함, 공간을 유연적으로 사용할 수 있음, 기본적으로 가능한 만큼 공간 차지 => ex)1fr 2fr ...
    * 높이를 지정하지 않으면 row에서 fr을 지정해도 0으로 인식
    * grid-template : 자식들의 grid-area 이름을 지정해주고 area와 같은 방식에 row값을 적어주고 마지막에 /(column)값 적어주면 됨, repeat은 적용되지 않음
- 8.Place Items
    * justify-items(수평), align-items(수직)의 속성은 부모에게 있음, 기본값은 strech, stretch가 아니면 자식들이 채워지지 않을 수 있음(기본크기를 지정하지 않고 text만 입력시)
    * justify-items : 수평을 기준으로 이동, 수직은 채워지지만 수평은 설정한 속성대로 적용
    * align-items : 수직을 기준으로 이동, 수평은 채워지지만 수직을 설정항 속성대로 적용
    * place-items : y x => 한번에 설정하기위해, y는 수직(align) x는 수평(justify)
- 9.Place Content
    * 전체 grid를 움직이는 방법, justify-content 와 align-content 가 있음
    * justify-content : 전체의 열(column)을 움직임
    * align-contens : 전체의 행(row)를 움직임
    * stetch(전체채움)을 사용하려면 크기를 px이 아닌 fr로 설정
    * place-content : y x =>한번에 설정, y(수직) x(수평) 
    * items -> box 하나하나에 적용, content -> grid전체에 적용
- 10.Auto Columns and Raows
    * align(justify)-self는 box개별적으로 속성을 줄 때 사용
    * place-self y/x: 한번에 설정
    * 설정한 row보다 가져온 data가 더 많을 경우 지정해준 범위 만큼만 값이 설정되고 나머지는 기본값
    * grid-auot-rows: (크기)를 사용하면 기존에 설정한 범위 이외의 나머지 범위의 값을 설정, 기존에 설정하지 않았으면 전체에 설정
    * grid-auto-flow : 원래는 자동으로 row값이 default 되지만 row가 아닌 다른 속성을 적용할 수 있음
    * grid-auto-columns : flow로 column를 지정하면 row로 정렬 되었던 box들이 column으로 정렬(flexbox에서 direction과 비슷)
- 11.minmax
    * element가 가능한한 크길 원하고 동시에 작게 되지 않길 원할때 사용
    * grid-template-column(row) : repeat(열행갯수,minmax(최소값,최대값))
    * 페이지를 줄이더라도 지정한 최소값 이하로는 줄어 들지 않음
- 12.auto-fit, auto-fill
    * element의 갯수를 알수 없고 무슨일이 일어날지는 알수 있을때 사용 => 반응형 디자인, 유동적인 것, 아이템에 대해서 잘 모를때 사용
    * auto-fill : 지정해준 사이즈만큼 열(column)을 만들어줌, element가 없더라도 지정해준 사이즈만큼 빈 공간이 만들어짐(row에다가 채워줌)
    * auto-fit : 지정한 element 갯수에 맞춰 크기를 늘려줌(row에 딱 맞게)
    * element의 사이즈를 그대로 하고 싶으면 fill, 늘려주고 싶으면 fit
- 13.min-comtent, max-content
    * box를 컨텐츠의 크기에 맞게 디자인
    * max-content : box를 컨텐츠에 필요한 만큼 커짐
    * min-content : box를 컨텐츠에 필요한 만큼 작아짐