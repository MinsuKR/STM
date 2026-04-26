<MX경로(win버전)>
C:\Users\User\AppData\Local\Programs\STM32CubeMX

<ST-linker(STSW-LINK009)>
https://www.st.com/en/development-tools/stsw-link009.html?utm_source=chatgpt.com#

<CLT 경로(win버전)>
https://www.st.com/en/development-tools/stm32cubeclt.html?icmp=tt38569_gl_lnkon_apr2024

<STM 데이터 시트>
https://os.mbed.com/platforms/ST-Nucleo-F303RE/

<cmake 설치 / ninza>
winget install Kitware.CMake
winget install Ninja-build.Ninja

<build하는법>
cmake --preset Debug (디버그 build 만들어줌)
cmake --build --preset Debug (build)

<처음 업로드> = 일반 SWD 연결(Normal mode
STM32_Programmer_CLI -c port=SWD -w build\Debug\<파일이름>.elf -v -rst
<다음 업로드 시 - 복구> = Under Reset 모드(=NRST 핀 = 이미 안에 저장된 펌웨어가 있어 리셋 후 업로드 해야 에러가 안뜸)
STM32_Programmer_CLI -c port=SWD mode=UR -w build\Debug\<파일이름>.elf -v -rst

<파일명 확인하기>
Get-ChildItem .\build\Debug\*.elf

Default comfiler/linker => GCC로

<빨간 줄 없애기>
CMake: Delete Cache and Reconfigure (ctrl + .)

<vscode 새로고침>
Developer: Reload Window (ctrl + ,)



다음주에 할거
1. 버튼 누르면 LED 점멸 시작, 다시 누르면 점멸 정지(timer)
2. 저항 가져오기, 모터, 스피커
3. UART
4. I2c


나중에 할거
1. 달력만들어서 LCD확인

0x41

1000 0010