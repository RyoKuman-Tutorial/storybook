# StoryBook

## front 에서 unit test 시에 사용할 수 있는 라이브러리

## 실행 방법

1. 스토리북 다운로드

   ```js
   `npx sb init`;
   ```

   위 경우 버전 충돌로 인하여 버전이 강제로 다운된다.<br/>
   때문에, yarn 을 사용하는걸 추천한다.<br/>

2. stories 작성
   테스트하고자 하는 컴포넌트의 스토리를 작성한다.<br/>

   ```js
   import React from "react";
   import Button from "./Button";

   export default {
     component: Button, // 테스트할 컴포넌트
     title: "button", // 테스트의 제목
   };

   const Template = (args) => <Button {...args} />;

   export const Default = Template.bind({});
   Default.args = {
     color: "red",
   }; // Deafault 라는 이름의 테스트는 Button 에 props 로 red 를 준, 테스트
   ```

3. 스토리북 실행

   ```js
   `start-storybook -p ${port number} -s public`
   ```

## 실행 결과

![다운로드](./img/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202022-12-13%20%EC%98%A4%ED%9B%84%201.33.12.png)
