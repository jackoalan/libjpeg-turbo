include_directories(.)
add_library(libjpeg-turbo
            turbojpeg.h turbojpeg.c
            jerror.c
            jutils.c
            jcparam.c
            jcapimin.c
            jcomapi.c
            jcapistd.c
            jdapistd.c
            jdapimin.c
            jdhuff.c
            jdatadst-tj.c
            jdatasrc-tj.c
            transupp.c
            jdtrans.c
            jctrans.c
            jcmaster.c
            jmemmgr.c
            jcmarker.c
            jcinit.c
            jdmaster.c
            jdmarker.c
            jdinput.c
            jdarith.c
            jdphuff.c
            jdcoefct.c
            jcarith.c
            jcphuff.c
            jchuff.c
            jmemnobs.c
            jccolor.c
            jcsample.c
            jcprepct.c
            jcdctmgr.c
            jccoefct.c
            jcmainct.c
            jquant1.c
            jquant2.c
            jdmerge.c
            jdcolor.c
            jdsample.c
            jdpostct.c
            jddctmgr.c
            jdmainct.c
            jsimd_none.c
            jfdctint.c
            jfdctfst.c
            jfdctflt.c
            jidctred.c
            jidctint.c
            jidctfst.c
            jidctflt.c
            jaricom.c)

if (NOT MSVC)
  target_compile_options(libjpeg-turbo PRIVATE -Wno-misleading-indentation
                         -Wno-unused-but-set-variable -Wno-unused-label
                         -Wno-implicit-fallthrough -Wno-attributes
                         -Wno-shift-negative-value)
endif()

target_include_directories(libjpeg-turbo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
