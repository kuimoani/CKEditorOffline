# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [TODO]
### Add
- Image Embeded 전환 기능 추가
  - ckeditor image dialog 커스터마이징?
  - image 선택시 전환여부 물어보는 레이어 창 띄우기?
  - 상단 메뉴나 아이콘버튼 만들어서 image 선택시 활성화 되게?
- images, video, link files Insert/DragDrop 기능 추가
  - 절대경로? 이미지 파일을 이동할 경우 짤림..여기저기 복사할때 문제됨
  - 상대경로? new file일때 상대경로로 할 수가 없음... 파일 삽입하면 강제저장하거나 일단 절대경로로 보여줬다가 저장할때 상대경로로?? html 직접 편집하는거면 일관성 없음
  - video는 http://ckeditor.com/addon/html5video 같은 addon 써야할듯... video tag 추가는 되는데 선택도 편집도 안됨..
- 스킨 동적 변환기능

### Change

## [Unreleased]
### Added
- image 파일 드래그앤드롭시 절대경로로 image 태그 연결해주는 기능 추가
- 모든 파일 드래그앤드롭시 절대경로로 a 태그 연결해주는 기능 추가

### Changed
- editor resize bug -> body show animation 삭제

## [0.1.3] - 2017-06-23
### Added
- Google Analytics 추가 -> GA는 Domain이 필수이므로 Firebase로 대체 -> Firebase는 거의 대부분 기능을 iOS와 Android만 지원... -> 다시 GA로.. 알아보니 도메인은 대충 적어도 된다고 함(참고:http://shibe97.hatenablog.com/entry/2017/01/17/094404, https://github.com/expo/electron-cookies)

### Changed
- document ready 대신 CKEDITOR.instanceReady 에서 window resize 하는 방식으로 개선
- 파일 New, Open시 ckeditor undo 히스토리 삭제
- File Open & Save Dialog를 Modal Window로 수정

## [0.1.2] - 2017-06-22
### Added

### Changed
- build script 수정 - electron-package 8.7.1 버전에 맞게 수정
- editor change event 문제 때문에 setTimeout 쓴 코드 정리
- beforeunload 에서 return false(cancel)가 잘 되지 않는 버그로 인해 Atom이나 VSCode처럼 temp 저장방식으로 개선하기 -> win.close 이벤트에서 dialog 띄우는 방식으로 해결
- Control+S 단축키로 저장했을 경우 "saved." 표시가 안되고 "modified."로 표시되는 문제 해결하기 (checkDirty() 활용?)
- Drag&Drop으로 파일오픈시 저장되지 않은 문서 있을 경우 Confirm 창 띄우기
- CKEditor -> HDoc 으로 이름 전환

## [0.1.1] - 2017-06-04
### Added
- add github
- packaging
- app icons : https://romannurik.github.io/AndroidAssetStudio/icons-launcher.html
- html file drag-drop
- window menu 정리 (단축키 포함)
- confirm [close window,new,open] when modified
  - 창 닫을때는 electron 버그로인해 dialog를 움직인 후 no, cancle 누르면 그냥 quit으로 넘어가버림..

### Changed
- clear text when new

## [0.1.0] - 2017-06-03
### Added
- ckeditor 4.7 init
- jquery 3.2.1 init : https://blog.outsider.ne.kr/1170
- bootstrap 3.3.7 init
- add new, open, save, save as
- editor resize
- text change event
- status message ui

### Changed
- bootstrap local install
