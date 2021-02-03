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