# <img src="https://github.com/uoyssim/ChosunTruck/blob/master/README/Logo.png?raw=true" width="64">조선트럭

## 소개
조선트럭은 [유로 트럭 시뮬레이터 2](https://eurotrucksimulator2.com/)를 위한 자동 주행 솔루션입니다.
최근, 자동 주행 기술은 큰 이슈이며 우리는 그것과 관련된 기술들을 공부하고 있습니다.
유로 트럭 시뮬레이터 2라는 시뮬레이트된 환경에서 개발되어 가상의 차량을 이용하여 연구할 수 있습니다.
이 시뮬레이터는 실제 도로와 유사한 테스트 환경을 제공하기 때문에 자동 주행 관련 기술들을 적용할 수 있습니다.

## 특징
* 시뮬레이터 내의 차량을 직접 조작하지 않고도 운전할 수 있습니다.
* 자동 주행의 기본적인 원리를 이해할 수 있습니다.
* 리눅스에서만 실험적으로 차량 인식을 할 수 있습니다.

## 실행 방법
### Windows

#### Dependencies
- 운영체제: Windows 7, 10 (64bit)

- IDE: Visual Studio 2013, 2015

- OpenCV version: >= 3.1

- [Cuda Toolkit 7.5](https://developer.nvidia.com/cuda-75-downloads-archive) (참고: ADVANCED 설치를 하시려면 Toolkit과 Visual Studio와 통합만 설치하세요. 드라이버와 다른 것들을 설치하지 마세요. 설치가 끝나면, 다음과 같은 프로젝트 속성을 볼 수 있습니다: https://i.imgur.com/e7IRtjy.png)

- 만약 설치 중 문제가 생기시면, 저희 저희 위키페이지에 있는 [Windows Installation wiki page](https://github.com/bethesirius/ChosunTruck/wiki/Windows-Installation)를 참고해주세요.

#### 윈도우에서 작동하기 위해 필요한 것들:
- **C:\Users\YOURUSERNAME\Documents\Euro Truck Simulator 2\profiles에 가서 controls.sii에 있는** 
```
config_lines[0]: "device keyboard `di8.keyboard`"
config_lines[1]: "device mouse `fusion.mouse`"
```
을 
```
config_lines[0]: "device keyboard `sys.keyboard`"
config_lines[1]: "device mouse `sys.mouse`"
```
로 변경해주세요.
(thanks Komat!)
- **While you are in controls.sii, make sure your sensitivity is set to:**
```
 config_lines[33]: "constant c_rsteersens 0.775000"
 config_lines[34]: "constant c_asteersens 4.650000"
```
#### 그 후:
- visual studio 프로젝트를 열어 빌드를 하세요. 
- 유로 트럭 시뮬레이터(ETS2)를 창모드로 실행시키고 해상도를 1024 * 768로 설정해주세요.(이것은 모니터 해상도가 1920 * 1080이고 유로트럭 시뮬레이터 2의 해상도가 1024 * 768일 때 잘 작동합니다.)

### 리눅스
#### Dependencies
- 운영체제: Ubuntu 16.04 LTS

- [OpenCV version: >= 3.1](http://embedonix.com/articles/image-processing/installing-opencv-3-1-0-on-ubuntu/)

- (선택적) Tensorflow version: >= 0.12.1

### 리눅스 파일 안에서 아래의 명령어를 사용하여 소스코드를 빌드해주세요.
```
make
```
### 만약 차량 인식을 원한다면:
````
make Drive
````
#### 그후:
- 유로 트럭 시뮬레이터(ETS2)를 창모드로 실행시키고 그것의 해상도를 1024 * 768로 조정해주세요.(이것은 모니터 해상도가 1920 * 1080이고 유로트럭 시뮬레이터 2의 해상도가 1024 * 768일 때 잘 작동합니다.)
- 유로 트럭 시뮬레이터2(ETS2) 창을 자동적으로 찾을 수 없어 유로 트럭 시뮬레이터2(ETS2) 창을 우측 하단 모서리에 맞춰 주세요.
- 유로 트럭 시뮬레이터2(ETS2) 설정 창에서, 컨트롤 방식을 'Keyboard + Mouse Steering'로 변경해주시고, '좌 클릭'을 가속으로, '우 클릭'을 브레이크로 설정해주세요.
- 고속 도로로 이동하셔서 트럭의 속도를 40~60km/h로 설정해주세요.(크루즈 모드를 사용하는 것이 속도를 맞추는 데 도움이 됩니다.)
- 프로그램을 실행해주세요!

#### 차량 인식 모드를 사용하고 싶으시면, -D 또는 --Car_Detection를 입력하세요.
```
./ChosunTruck [-D|--Car_Detection]
```
## 문제 해결
저희 [위키 페이지](https://github.com/bethesirius/ChosunTruck/wiki/Troubleshooting)를 참조해주세요.

만약 이 프로그램을 실행시키는 데 문제가 있으시다면, 아래의 비디오를 참조하거나, [새로운 이슈](https://github.com/bethesirius/ChosunTruck/issues)를 열어 저희 팀에 알려주세요.

## 데모 비디오
차선 인식 (Youtube link)

[![youtube link](http://img.youtube.com/vi/vF7J_uC045Q/0.jpg)](http://www.youtube.com/watch?v=vF7J_uC045Q)
[![youtube link](http://img.youtube.com/vi/qb99czlIklA/0.jpg)](http://www.youtube.com/watch?v=qb99czlIklA)

차선 인식 + 차량 인식 (Youtube link)

[![youtube link](http://img.youtube.com/vi/w6H2eGEvzvw/0.jpg)](http://www.youtube.com/watch?v=w6H2eGEvzvw)

## Founders
- 송치완, chi3236@gmail.com

- 심재철, simjaecheol@naver.com

- 추성준, hs4393@gmail.com

## Contributors
- [zappybiby](https://github.com/zappybiby)

## 기여하는 방법
이 프로젝트에 관심있는 어느 누구라도 환영합니다. 이 프로젝트를 포크하셔서 pull request를 날려주세요.

## 라이센스
ChosunTruck, Euro Truck Simulator 2 auto driving solution
Copyright (C) 2017 chi3236, bethesirius, uoyssim

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
