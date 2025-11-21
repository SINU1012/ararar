# Site Preview AR Overlay

모바일 브라우저에서 바닥/테이블을 인식해 `site_preview.png`(1000x545)를 3D 평면으로 띄우는 WebXR AR 데모입니다. Android 크롬에서 WebXR AR을 지원하며, HTTPS 환경에서 동작합니다. (iOS Safari WebXR 미지원 시에는 안내만 표시)

## 실행 방법
1) 프로젝트 루트에서 정적 서버 실행  
   - `python3 -m http.server 8000`  
   - 또는 `npx serve .`  
2) 휴대폰 크롬에서 `https://<호스트>:8000` 혹은 배포 URL 접속 (로컬은 `https://<LAN IP>:8000` 권장).  
3) **AR 시작** 버튼 → 카메라 허용 → 바닥/테이블이 감지되면 보라색 링이 나타납니다.  
4) 화면을 탭하면 그 위치에 사이트 프리뷰 이미지가 배치됩니다. 다시 탭하면 새 위치로 이동합니다.

## 특징
- Three.js WebXR hit-test로 바닥면 감지 후 2D 이미지를 더블사이드 평면으로 표시
- 이미지 비율 유지(너비 약 1.2m, 높이 자동 비례)
- 지원되지 않는 브라우저에서는 안내 문구로 대체

## 주의사항
- WebXR AR은 HTTPS + Android 크롬 최신 버전에서 동작합니다.  
- iOS Safari는 WebXR이 없어 AR 버튼이 표시되지 않을 수 있습니다(미래 버전에서 지원 시 자동 활성화).  
- GH Pages/Netlify 등 HTTPS 호스팅으로 배포하면 QR 코드로 스캔해 바로 테스트할 수 있습니다.
