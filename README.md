### Protog | Protocol Buffer에서의 고급문법 지원을 위한 확장기술

AS..IS..
- Protocol Buffer는 제네릭, Nullable과 같은 스팩을 구현하기 힘듭니다.
- 제네릭의 경우 아예 구현이 불가능하며, Nullable한 메세지를 argument/return type으로 사용하기 위해서는 별도 타입을 지정해야합니다.

TO..BE..
- `.protog` 라는 별도 확장자 파일을 통해, protocol buffer의 스팩을 명시할 수 있습니다.
- `.protog`는 Protog의 확장된 문법을 따르며, 이는 Generic, Nullable Argument/Return type등의 문법을 지원합니다.
- .protog파일은 `generateProtog`라는 별도의 사전작업을 통해, .proto파일의 집합으로 트랜스파일링할 수 있습니다.
- 개발자는 이제, generic등의 고급문법을 사용하기 위해 protog파일을 작성하며, 자동화된 테스크를 통해 이를 proto파일로 트랜스파일링한 뒤 사용할 수 있습니다.
