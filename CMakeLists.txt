cmake_minimum_required(VERSION 3.20)
set(CMAKE_Fortran_COMPILER "E:/IntelSWTools/compilers_and_libraries_2020.4.311/windows/bin/intel64/ifort.exe")
set(ENV{LIB} "E:/IntelSWTools/compilers_and_libraries_2020.4.311/windows/compiler/lib/intel64_win;F:/Program Files (x86)/Microsoft Visual Studio/2017/Community/VC/Tools/MSVC/14.16.27023/lib/x64;F:/Windows Kits/10/Lib/10.0.17763.0/um/x64;F:/Windows Kits/10/Lib/10.0.17763.0/ucrt/x64;F:/Windows Kits/10/Lib/10.0.17763.0/um/x64")
set(ENV{Path} "E:/IntelSWTools/compilers_and_libraries_2020.4.311/windows/bin/intel64;$ENV{Path}")  # 添加xilink 可能还需要添加环境变量

project(ftest Fortran)

message($ENV{Path})  # 看看你狗日的加了什么狗屁环境变量

enable_language(Fortran)
link_directories("E:/IntelSWTools/compilers_and_libraries_2020.4.311/windows/compiler/lib/intel64_win")
link_directories("E:/IntelSWTools/compilers_and_libraries_2020.4.311/windows/redist/intel64_win/compiler")  # 这个目录全是狗日的dll debug要用 找不到就tm复制过来
add_executable(ftest main.f90)
