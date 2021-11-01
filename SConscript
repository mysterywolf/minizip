from building import *

cwd = GetCurrentDir()
src	= Glob('*.c')

CPPPATH = [cwd]

group = DefineGroup('minizip', src, depend = ['PKG_USING_MINIZIP'], CPPPATH = CPPPATH)

Return('group')
