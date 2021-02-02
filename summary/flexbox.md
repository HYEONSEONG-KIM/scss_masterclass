# FlexBox :
0. Life Before FlexBox
- diplay 중 inline은 옆으로 정렬이며,Box가아닌 element이고 유동적인 것으로 너비와 높이가 없음
- inline-block은 block속성을 유지(너비와 높이가 있음)
- 같은 box들 중 특정 box를 지정하고 싶으면 .(ClassName):nth-child(숫자)
1. First Rule of FlexBox
- flexbox에서는 children을 얘기하지 않음
- 무언가를 움직이고 싶다면 flexbox container안에 있어야함
- 부모에 flex를 주고 바로 붙어있는 자식만 적용
- 즉, 항상 붙어있는 부모가 자식의 위치를 움직일 수 있음
2. Main Axis and Cross Axis
- flex container의 flex-direction 기본값은 row
- diretion이 row : horizontal axis(수평축)이 main axis(axis-중심선)=>가로, vertical axis(수직축)이 cross axis=>세로
- main axis 방향으로 item을 옮기기 위해서는 justify-content 사용
- cross axis 방향으로 item을 옮기기 위해서는 align-itmes 사용
3. Column and Row
- direction이 column : main axis가 세로,cross axis가 가로(row와 반대)
- column 과 row가 바뀌더라도 main axis=>justify-content, cross axis는 align-itmes 사용
4. align-self and order
- align-self는 align-items와 비슷한 일을 하지만 한 box에만 해당
- 부모에게 높이가 없다면 모두 가운데 있게 됨(row에서 cross axis가 세로)
- order는 HTML을 변경할 수 없을때 box의 순서를 변경할 경우 사용
- box의 order 기본값은 0, 해당 박스의 order값을 변경해주면 변경된 숫자 순서로 정렬