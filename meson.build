# ffplay original ffmpeg ver 4.4

project('ffplay', 'c',
	version: '4.4',
  default_options: ['warning_level=0'])

cc = meson.get_compiler('c')
dep_libm = cc.find_library('m')

libavcodec = dependency('libavcodec')
libavutil = dependency('libavutil')
libswresample = dependency('libswresample')
libavformat = dependency('libavformat')
libswscale = dependency('libswscale')
libavfilter = dependency('libavfilter')
libavdevice = dependency('libavdevice')

SDL2 = dependency('SDL2')

includes = include_directories('.')
  
executable(
    'ffplay', [
	'ffplay.c',
	'cmdutils.c'
    ],
    include_directories: [includes],  # インクルードディレクトリの指定
	dependencies : [dep_libm,libavcodec,libavutil,libswresample,libavformat,libswscale,libavfilter,libavdevice,SDL2])
