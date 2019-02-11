## Jest
- 자바스크립트 테스트 프레임워크
- 테스트 러너

![default](https://user-images.githubusercontent.com/14510347/52565466-37cab580-2e4a-11e9-84fd-a2515b4c0c72.png)


- * The Front-End Tooling Survey 2018 - Results - AshleyNolan.co.uk - Blog and Portfolio for Ashley Nolan
![45228080-24e11180-b2fd-11e8-9b72-f8a5b0e8d9fc](https://user-images.githubusercontent.com/14510347/52565725-03a3c480-2e4b-11e9-9345-85bc456698f3.png)


```javascript
// Story
describe('PhoneInputScreen 컴포넌트', () => {
// Senario
  describe('PhoneInputScreen 컴포넌트를 생성할 수 있다.', () => {
    it('설정없이 PhoneInputScreen을 생상하면, default state를 가진 PhoneInputScreen을 생성한다.', () => {
      // Given
      const expected = {
        phoneNumber: undefined,
        qualified: false,
        isRequestSent: false,
        errorMessage: '',
        borderColor: cColor.coolBlack,
      }
      
      // When
      const wrapper = shallow(<PhoneInputScreen />);
     
      // Then
      expect(wrapper.state()).toEqual(expected);
    });
  });
});

```


