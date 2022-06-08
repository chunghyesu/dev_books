일상 속 사물이 알려주는 웹 API 디자인       \
<저자 아노드 로렛 / 번역 황건구>
-------------------------------------------

### 4. API 명세 포맷을 이용한 API디자인    
API의 세부사항을 표현하기 위한 데이터 포맷. 파일 자체가 데이터를 구조화해서 포함하고 있으므로 프로그램이 파일을 읽을 수 있고, 다른 무언가로 변환하기도 쉬움
```
/products:
  description: Catalog
  post:
    description: Add product to catalog
    requestBody:
      description: Product
      content: 
        application/json:
          schema:
            properties:
              name:
                type: string
                example: The Design of Web APIs
              price:
                type: number
                example: 44.99
```
* OAS[OpenAPI Specification](이전에 스웨거(Swagger)라고 불림)
- 프로그래밍 언어에 상관없이 사용하는 REST API 명세 포맷
- YAML 포맷 사용
- RAML, Blueprint 등 유사 포맷 존재
- 온라인 스웨거 에디터(http://editor.swagger.io)
- API의 프로그래밍적인 표현과 데이터에 대해서 충분한 디자인을 거친 이후에 사용해야한다.

## 2. 사용하기 좋은 API디자인
컨슈머 관점에 초점을 맞추고 사용자를 염두해 두고 설계하면서 선택한 표현이 합리적인지 그리고 컨슈머가 쉽게 이해할 수 있는지 고려.
- 일상적 약어 외에는 좋은 표현이 아님.(+ 이름을 정할때는 세단어에서 두 단어의 조합까지만 한기를 권함.
- 적절한 데이터 포맷 선택. 

