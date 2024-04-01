# week02 yolo_nas_practice

📖목표
- 이미지 라벨링 및 학습 데이터 생성
- yolo_nas 학습 모델 제작 및 테스트

<details>
  <summary>🏆학습 과정</summary>
  <div>
    <ul>
      <li>1. 이미지 라벨링 <br />
        (1) Roboflow를 통해 cat & dog 이미지 라벨링</li>
      <li>2. 라이브러리 설치 및 import & gpu 설정(학습 과정에서 cpu만으로는 ram 메모리 부족)</li>
      <li>3. 학습 모델 checkpoint 생성 및 라벨링 이미지 불러오기</li>
      <li>4. 이미지 데이터 분류 및 파라미터 설정</li>
      <li>5. 모델 인스턴스화(s, l, m 중 s와 l 모델로 테스트) <br /> 
        (1) 초기 모델은 s모델로 시작 <br />  
        (2) 모델 완성 후 테스트 과정에서 l모델로 변경 </li>
      <li>6. 모델 학습에 필요한 파라미터 설정 <br />
        (1) 학습 과정에서 max_epoch 변수 값 변경(10 -> 15 -> 20 -> 100) <br />
        (2) 각 반복 횟수별로 detection 확인</li>
      <li>7. 모델링 시작</li>
      <li>8. 최적 모델 확인 <br />
        (1) 지정해둔 checkpoint의 pth파일을 통해 최적의 모델 확인</li>
      <li>9. 최적 모델 테스트 결과 확인</li>
      <li>10. 새로운 이미지로 detection 확인</li>
    </ul>
  </div>
</details>

🥉최종 결과  <div></div> ![image](https://github.com/gyuchangShim/yolo_nas_practice/assets/132640569/24d2bd3f-ef39-43b7-bbf0-8f58ec812b57)

<hr />

### 📎학습 과정에서 아쉬운 점
*1. 너무 적은 학습 데이터* <br />
> 초기 데이터 라벨링을 진행할 때 cat & dog 이미지를 각각 20장으로 설정했다. 초기에는 간단한 detection 모델이기 때문에 총 40장의 데이터로 결과를 얻을 수 있지 않을까 생각했지만 최종 결과를 확인해보니 학습 데이터 자체가 너무 적어 모델링 과정에서 충분한 학습이 되지 않은 점이 가장 아쉽다.


*2. 학습 과정에서의 환경* <br />
> 초기 모델링을 생각했을 때 cpu환경으로 가능할 것이라 판단해 노트북의 pycharm으로 모델링을 시작했지만 실제로 학습 과정에서 너무 오랜 시간 학습하게 되는 문제가 있어 colab 환경으로 옮겨 과제를 이어나갔다. colab의 gpu환경으로 cpu보다는 더 빠르게 학습이 가능했지만 이미지 데이터나 반복 횟수(epoch)가 지금보다 더 많아질 경우 colab에서도 시간이 꽤 걸릴것 같다고 생각하게 됬고 다음 과제나 프로젝트는 내장 gpu가 있는 환경에서 진행해야 된다고 생각했다.


<hr />
✏️Reference <br />
 이미지 라벨링 및 모델링: https://jypark1111.tistory.com/64 <br />
 파라미터 지정 및 모델링: https://youtu.be/vfQYRJ1x4Qg <br />
<br />
 💻TODO : confusion matrix(loss graph) 확인
