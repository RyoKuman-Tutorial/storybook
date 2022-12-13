# StoryBook

## front 에서 unit test 시에 사용할 수 있는 라이브러리

## 사용 방법

1. npx sb init 사용
   위 경우 버전 충돌로 인하여 버전이 강제로 다운된다.
   때문에, yarn 을 사용하는걸 추천한다.

2. stories 작성
   테스트하고자 하는 컴포넌트의 스토리를 작성한다.

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
