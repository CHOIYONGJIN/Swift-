# **Swift** 정리  
## *집합(datatype?)*
typealias: datatype의 별칭
### tuple = (1, "one", "일") 등으로 활용가능
접근: tuple.0
print(tuple.0 = 1)
### 컬렉션
* **Array**: 순서를 가진 한 종류의 데이터타입의 집합
    선언 방법: Array<String> or [String]
        ex) var meetingRooms: Array<String> = ["Revera", "matissa"]
        추가: meetingRooms += ["hissape"] or speed.append(Int(114.1))
    index이용해 추가, 값을 가져옴
        ex) meetingRooms[1], speed.first, speed.last
    복사형식이기때문에 같은 배열을 할당하여 하나의 값을 변경하면 두 배열은 달라진다.
* **Dictionary**: *Key*와 *value*가 대응되는 것들의 집합
    선언 방법: var roomCapacity: [String: Int]= ["Revera": 10, "matissa": 8,             "hissape": 20]
    추가: ~~roomCapacity += ["Renoir": 40]~~
        value를 key에 할당하는 방식으로 추가함
        ex) roomCapacity["Renoir"] = 40
    값 확인: roomCapacity["Revera"]
        **let roomNames = meetingRooms.keys 로 하면 LazyMapCollection 형태로 나옴 --> let roomNames = [String](meetingRooms.keys) 형태로 함**
* **Set**: ~~순서~~, 집합 --> 여러 집합 연산을 사용
    **집합 연산기호들**
    * intersection()
    * subtract()
    * union()
    * exclusiveOr()