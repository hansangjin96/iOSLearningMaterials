# 데이터 압축 기술
1. 아날로그 신호를 디지털 신호로 변환하려면 주기적으로 값을 수집하는 샘플링, 샘플링 된 값을 특정한 값으로 바꾸는 양자화 를 진행해야함
2. 압축 기법에는 손실 압축과 비손실 압축이 있고
    * 손실 압축은 인간이 지각하기 힘든 범위의 데이터를 버리는 것
    * 비손실 압축은 원본파일 유지, 손실압축보다 압축율이 떨어짐
        * 허프만 코딩은 무손실 압축으로 데이터 문자의 등장 빈도에 따라 다른 길이를 부여
1. URL인코딩이란 퍼센트 인코딩이라고도 불리며 % 뒤에 아스키 코딍의 hex값을 붙여준것
1. ZIP이란 필 캐츠가 만든 무손실 압축 포맷, 확장자가 아닌 컨테이너 포맷이며 Deflate알고리즘 사용
    * 7z : 오픈소스 압축 프로그램으로 자유 소프트웨어, 대중화,멀티코어에서 빠른 속도, 높은 압축율등의 장점이 있음
    * RAR : 압축율, 속도, 분할 압축 기능, 리커버리 레코드 등으로 인기, 7z와 같이 사용 (대용량을 보낼때 rar이 유리)
1. 중첩의 원리 - FT - DCT : 오디오, 영상 등의 압축 기법에서 사용된다.(얼마나 깊이 조사해야하는지 잘 모르겠습니다..)

# 이미지
1. 표현방식
    * 비트맵 방식 : 픽셀단위로 그림을 표현, 계단현상, 용량이 크고 처리속도가 느림
    * 벡터 방식 : 점, 선, 곡선, 다각형 등을 사용해 그림을 나타냄 , 확대, 이동, 회전 등에서 그림의 품질이 저하되지 않음
1. 종류
    * BMP : 비트맵 이미지를 저장하는데 쓰이는 파일 포맷, 크기가 크고 압축이 안되어있음
    * JEPG : 그림을 표현하기 위한 손실/비손실 압축 표준 , .jpg , .jpeg, .jpe등의 확장자가 있음, 작은 용량으로 널리 사용
    * PNG : 무손실 압축 포맥, GIF보다 많은 색(32비트) 표현 가능
    * GIF : 무손실 압축 포맷, jpg가 나오면서 Animated GIF(움짤) 외에는 잘 사용되지 않는다
    * DNG : 어도비가 개발한 RAW미디어 포맷, .dng확장자를 가짐
    * RAW : 가공되지 않은 디지털 데이터, 전문가 레벨에서 주로 사용, 확장자가 .raw가 아님
    * SVG : 2차원 벡터 그래픽을 표현하기 위한 XML기반의 파일형식 , CSS를 이용해 다양한 효과를 줄 때 사용

# 오디오
1. PCM : 아날로그 신호를 샘플링, 양자화, 엔코딩 해서 0과 1의 디지털 신호로 표현하는 방식
1. WAVE : 윈도우에서 표준적으로 사용되는 PCM파일, 무손실 무압축 파일, 이미지 파일의 RAW파일과 비슷, 프로그래머에게 유리
1. MP3 : 97년 등장한 손실 압축 포맷, 이후 더 발전된 AAC 등장
1. OGG : MP3보다 용량 대비 음질이 뛰어난 컨테이너 포맷, .ogv, .oga, .ogx, .ogg, .spx, .opus, .flac등의 확장자가 있음, FLAC이 가장 유명
1. FLAC : 무손실 압축 포맷, 자유 소프트웨어, 다른 무손실 압축에 비해 압축률이 낮지만 속도가 빠름

# 비디오
1. 코덱 & 컨테이너
    * 코덱 : 코더 & 디코더, 영상신호를 디지털 신호로 변환하고(인코딩), 디지털 신호를 영상신호로 변환하는 것(디코딩)
    * 컨테이너 : 코덱으로 압축된 미디어 + 코덱 이름 제목 아티스트 등의 메타데이터
1. H.264/265
    * H.264 : 2003년 발표된 동영상 표준, AVC라고도 불리며 기존 MPEG-4 Part 2보다 발전
    * H.265 : 13년 발표, HEVC라고 불림, 압축효율이 높음, 라이센스가 비싸고 좋은 CPU필요
    * H.266 :  H.265의 후속작으로 초고해상도 영상처리용으로 개발
1. VP9/10
    * VP9 : 2012년 구글이 개발한 무료 오픈소스 비디오 코덱, 압축율이 높아지고 화질 개선이 큼
    * AV1(VP10) : 18년 오픈 미디어 연합(Alliance for Open Media)이 개발, 데이터 레이트 절감, 인코딩 시간이 길고 안정화 최적화가 안되어있음
1. MP4 vs AVI
    * MP4 : 동영상 전문가 그룹(MPEG)에서 내놓은 동영상 파일 형식. 국제 표준이기 때문에 정한 몇가지의 코덱만을 사용
    * AVI : 92년 마소에서 개발한 거의 모든 종류의 코덱을 담을 수 있는 컨테이너 포맷
    * MKV : 가장 진보된 컨테이너 포맷 ,오픈소스, 개수 제한없이 파일을 담을 수 있고 기능이 많음