AC_INIT([enigma2-oe-alliance-plugins],[1.0])
AM_INIT_AUTOMAKE([dist-bzip2 foreign no-define tar-pax])
AC_CONFIG_HEADERS([enigma2-plugins-config.h])

# Silent rules are available since 1.11, but older versions
# are still in use. So don't use them unconditionally.
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

AC_USE_SYSTEM_EXTENSIONS
AC_SYS_LARGEFILE

AC_PROG_CC
AC_PROG_CXX
m4_ifdef([LT_INIT], [LT_INIT], [AC_PROG_LIBTOOL])
AC_CONFIG_MACRO_DIR([m4])

AC_CHECK_HEADERS([dbox/fp.h dbox/lcd-ks0713.h])

AC_PATH_PROG(MSGFMT, msgfmt, AC_MSG_ERROR(Could not find msgfmt))

AM_PATH_PYTHON
AX_PYTHON_DEVEL
AX_PTHREAD

AC_ARG_WITH(boxtype,
	[  --with-boxtype=NAME box type [[none,dm7025,dm800...]]],
	[BOXTYPE="$withval"],[BOXTYPE="dm800"])
AC_SUBST(BOXTYPE)
AC_DEFINE_UNQUOTED(BOXTYPE,"$BOXTYPE",[box type])

AC_ARG_WITH(oever,
	[  --with-oever=NAME oe name [[7.1,...]]],
	[OE_VER="$withval"],[OE_VER=""])
AC_SUBST(OE_VER)
AC_DEFINE_UNQUOTED(OE_VER,"$OE_VER",[oe name])

AC_ARG_WITH(boxbrand,
	[  --with-boxbrand=NAME box brand [[dreambox,...]]],
	[BOXBRAND="$withval"],[BOXBRAND=""])
AC_SUBST(BOXBRAND)
AC_DEFINE_UNQUOTED(BOXBRAND,"$BOXBRAND",[box brand])

AC_ARG_WITH(distro,
	[  --with-distro=NAME distro name [[openvix,openatv,...]]],
	[DISTRO="$withval"],[DISTRO="egami"])
AC_SUBST(DISTRO)
AC_DEFINE_UNQUOTED(DISTRO,"$DISTRO",[distro name])

AC_ARG_WITH(imagetype,
	[  --with-imagetype=NAME imagetype name [[release,developer,...]]],
	[DISTRO_TYPE="$withval"],[DISTRO_TYPE="release"])
AC_SUBST(DISTRO_TYPE)
AC_DEFINE_UNQUOTED(DISTRO_TYPE,"$DISTRO_TYPE",[imagetype name])

AC_ARG_WITH(arch,
	[  --with-arch=NAME arch name [[mipsel32,sh4...]]],
	[ARCH_TYPE="$withval"],[ARCH_TYPE="mipsel32"])
AC_SUBST(ARCH_TYPE)
AC_DEFINE_UNQUOTED(ARCH_TYPE,"$ARCH_TYPE",[arch name])

AC_ARG_WITH(display-type,
	[  --with-display-type=NAME display type [[7segment,textlcd...]]],
	[DISPLAY_TYPE="$withval"],[DISPLAY_TYPE="textlcd"])
AC_SUBST(DISPLAY_TYPE)
AC_DEFINE_UNQUOTED(DISPLAY_TYPE,"$DISPLAY_TYPE",[display type])

AC_ARG_WITH(flash-type,
	[  --with-flash-type=NAME flash type [[smallflash,...]]],
	[HAVE_SMALLFLASH="$withval"],[HAVE_SMALLFLASH="true"])
AC_SUBST(HAVE_SMALLFLASH)
AC_DEFINE_UNQUOTED(HAVE_SMALLFLASH,"$HAVE_SMALLFLASH",[smallflash])

AC_ARG_WITH(hdmi,
	[  --with-hdmi=NAME hdmi [[hdmi......]]],
	[HAVE_HDMI="$withval"],[HAVE_HDMI="true"])
AC_SUBST(HAVE_HDMI)
AC_DEFINE_UNQUOTED(HAVE_HDMI,"$HAVE_HDMI",[hdmi])

AC_ARG_WITH(yuv,
	[  --with-yuv=NAME yuv [[yuv......]]],
	[HAVE_YUV="$withval"],[HAVE_YUV="true"])
AC_SUBST(HAVE_YUV)
AC_DEFINE_UNQUOTED(HAVE_YUV,"$HAVE_YUV",[yuv])

AC_ARG_WITH(rca,
	[  --with-rca=NAME rca [[rca......]]],
	[HAVE_RCA="$withval"],[HAVE_RCA="true"])
AC_SUBST(HAVE_RCA)
AC_DEFINE_UNQUOTED(HAVE_RCA,"$HAVE_RCA",[rca])

AC_ARG_WITH(av-jack,
	[  --with-av-jack=NAME av-jack [[av-jack......]]],
	[HAVE_AV_JACK="$withval"],[HAVE_AV_JACK="true"])
AC_SUBST(HAVE_AV_JACK)
AC_DEFINE_UNQUOTED(HAVE_AV_JACK,"$HAVE_AV_JACK",[av-jack])

AC_ARG_WITH(scart,
	[  --with-scart=NAME scart [[scart......]]],
	[HAVE_SCART="$withval"],[HAVE_SCART="true"])
AC_SUBST(HAVE_SCART)
AC_DEFINE_UNQUOTED(HAVE_SCART,"$HAVE_SCART",[scart])

AC_ARG_WITH(scart-yuv,
	[  --with-scart-yuv=NAME scart-yuv [[scart-yuv......]]],
	[HAVE_SCART_YUV="$withval"],[HAVE_SCART_YUV="true"])
AC_SUBST(HAVE_SCART_YUV)
AC_DEFINE_UNQUOTED(HAVE_SCART_YUV,"$HAVE_SCART_YUV",[scart-yuv])

AC_ARG_WITH(dvi,
	[  --with-dvi=NAME dvi [[dvi......]]],
	[HAVE_DVI="$withval"],[HAVE_DVI="true"])
AC_SUBST(HAVE_DVI)
AC_DEFINE_UNQUOTED(HAVE_DVI,"$HAVE_DVI",[dvi])

AC_ARG_WITH(minitv,
	[  --with-minitv=NAME minitv [[minitv......]]],
	[HAVE_MINITV="$withval"],[HAVE_MINITV="true"])
AC_SUBST(HAVE_MINITV)
AC_DEFINE_UNQUOTED(HAVE_MINITV,"$HAVE_MINITV",[minitv])

AC_ARG_WITH(hdmi-in-hd,
	[  --with-hdmi-in-hd=NAME hdmi-in-hd [[hdmi-in-hd......]]],
	[HAVE_HDMI_IN_HD="$withval"],[HAVE_HDMI_IN_HD="true"])
AC_SUBST(HAVE_HDMI_IN_HD)
AC_DEFINE_UNQUOTED(HAVE_HDMI_IN_HD,"$HAVE_HDMI_IN_HD",[hdmi-in-hd])

AC_ARG_WITH(hdmi-in-fhd,
	[  --with-hdmi-in-fhd=NAME hdmi-in-fhd [[hdmi-in-fhd......]]],
	[HAVE_HDMI_IN_FHD="$withval"],[HAVE_HDMI_IN_FHD="true"])
AC_SUBST(HAVE_HDMI_IN_FHD)
AC_DEFINE_UNQUOTED(HAVE_HDMI_IN_FHD,"$HAVE_HDMI_IN_FHD",[hdmi-in-fhd])

AC_ARG_WITH(wol,
	[  --with-wol=NAME wol [[wol......]]],
	[HAVE_WOL="$withval"],[HAVE_WOL="true"])
AC_SUBST(HAVE_WOL)
AC_DEFINE_UNQUOTED(HAVE_WOL,"$HAVE_WOL",[wol])

AC_ARG_WITH(wwol,
	[  --with-wwol=NAME wwol [[wwol......]]],
	[HAVE_WWOL="$withval"],[HAVE_WWOL="true"])
AC_SUBST(HAVE_WWOL)
AC_DEFINE_UNQUOTED(HAVE_WWOL,"$HAVE_WWOL",[wwol])

AC_ARG_WITH(transcoding,
	[  --with-transcoding=NAME transcoding [[transcoding,...]]],
	[HAVE_TRANSCODING="$withval"],[HAVE_TRANSCODING="true"])
AC_SUBST(HAVE_TRANSCODING)
AC_DEFINE_UNQUOTED(HAVE_TRANSCODING,"$HAVE_TRANSCODING",[transcoding])

AC_ARG_WITH(multitranscoding,
	[  --with-multitranscoding=NAME multitranscoding [[multitranscoding,...]]],
	[HAVE_MULTITRANSCODING="$withval"],[HAVE_MULTITRANSCODING="true"])
AC_SUBST(HAVE_MULTITRANSCODING)
AC_DEFINE_UNQUOTED(HAVE_MULTITRANSCODING,"$HAVE_MULTITRANSCODING",[multitranscoding])

AC_ARG_WITH(ci,
	[  --with-ci=NAME ci [[ci......]]],
	[HAVE_CI="$withval"],[HAVE_CI="true"])
AC_SUBST(HAVE_CI)
AC_DEFINE_UNQUOTED(HAVE_CI,"$HAVE_CI",[ci])

AC_ARG_WITH(machinebuild,
	[  --with-machinebuild=NAME build name [[inihdx,inihdp,...]]],
	[MACHINE_BUILD="$withval"],[MACHINE_BUILD="inihdx"])
AC_SUBST(MACHINE_BUILD)
AC_DEFINE_UNQUOTED(MACHINE_BUILD,"$MACHINE_BUILD",[build name])

AC_ARG_WITH(machinemake,
	[  --with-machinemake=NAME build name [[ventonhdx,vusolo,...]]],
	[MACHINE_MAKE="$withval"],[MACHINE_MAKE="ventonhdx"])
AC_SUBST(MACHINE_MAKE)
AC_DEFINE_UNQUOTED(MACHINE_MAKE,"$MACHINE_MAKE",[build name])

AC_ARG_WITH(machinename,
	[  --with-machinename=NAME machine name [[Solo,Ultimo,...]]],
	[MACHINE_NAME="$withval"],[MACHINE_NAME="Ultimo"])
AC_SUBST(MACHINE_NAME)
AC_DEFINE_UNQUOTED(MACHINE_NAME,"$MACHINE_NAME",[machine name])

AC_ARG_WITH(brandoem,
	[  --with-brandoem=NAME brand oem [[DAGS,DMM,...]]],
	[BRAND_OEM="$withval"],[BRAND_OEM="dags"])
AC_SUBST(BRAND_OEM)
AC_DEFINE_UNQUOTED(BRAND_OEM,"$BRAND_OEM",[brand oem])

AC_ARG_WITH(imageversion,
	[  --with-imageversion=NAME version number [[3.0]]],
	[IMAGEVERSION="$withval"],[IMAGEVERSION=""])
AC_SUBST(IMAGEVERSION)
AC_DEFINE_UNQUOTED(IMAGEVERSION,"$IMAGEVERSION",[version number])

AC_ARG_WITH(imagebuild,
	[  --with-imagebuild=NAME build number [[628]]],
	[IMAGEBUILD="$withval"],[IMAGEBUILD=""])
AC_SUBST(IMAGEBUILD)
AC_DEFINE_UNQUOTED(IMAGEBUILD,"$IMAGEBUILD",[build number])

AC_ARG_WITH(imagedevbuild,
	[  --with-imagedevbuild=NAME dev build number [[628]]],
	[IMAGEDEVBUILD="$withval"],[IMAGEDEVBUILD=""])
AC_SUBST(IMAGEDEVBUILD)
AC_DEFINE_UNQUOTED(IMAGEDEVBUILD,"$IMAGEDEVBUILD",[build number])

AC_ARG_WITH(feedsurl,
	[  --with-feedsurl=NAME feeds url  [[628]]],
	[FEEDSURL="$withval"],[FEEDSURL=""])
AC_SUBST(FEEDSURL)
AC_DEFINE_UNQUOTED(FEEDSURL,"$FEEDSURL",[feeds url ])

AC_ARG_WITH(imagedir,
	[  --with-imagedir=NAME imagedir folder [[628]]],
	[IMAGEDIR="$withval"],[IMAGEDIR=""])
AC_SUBST(IMAGEDIR)
AC_DEFINE_UNQUOTED(IMAGEDIR,"$IMAGEDIR",[imagedir folder])

AC_ARG_WITH(imagefs,
	[  --with-imagefs=NAME imagefs folder [[628]]],
	[IMAGE_FSTYPES="$withval"],[IMAGE_FSTYPES=""])
AC_SUBST(IMAGE_FSTYPES)
AC_DEFINE_UNQUOTED(IMAGE_FSTYPES,"$IMAGE_FSTYPES",[imagefs folder])

AC_ARG_WITH(mtdrootfs,
	[  --with-mtdrootfs=NAME mtdrootfs number [[628]]],
	[MTD_ROOTFS="$withval"],[MTD_ROOTFS=""])
AC_SUBST(MTD_ROOTFS)
AC_DEFINE_UNQUOTED(MTD_ROOTFS,"$MTD_ROOTFS",[mtdrootfs number])

AC_ARG_WITH(mtdkernel,
	[  --with-mtdkernel=NAME mtdkernel number [[628]]],
	[MTD_KERNEL="$withval"],[MTD_KERNEL=""])
AC_SUBST(MTD_KERNEL)
AC_DEFINE_UNQUOTED(MTD_KERNEL,"$MTD_KERNEL",[mtdkernel number])

AC_ARG_WITH(rootfile,
	[  --with-rootfile=NAME rootfile name [[628]]],
	[ROOTFS_FILE="$withval"],[ROOTFS_FILE=""])
AC_SUBST(ROOTFS_FILE)
AC_DEFINE_UNQUOTED(ROOTFS_FILE,"$ROOTFS_FILE",[rootfile name])

AC_ARG_WITH(kernelfile,
	[  --with-kernelfile=NAME kernelfile name [[628]]],
	[KERNEL_FILE="$withval"],[KERNEL_FILE=""])
AC_SUBST(KERNEL_FILE)
AC_DEFINE_UNQUOTED(KERNEL_FILE,"$KERNEL_FILE",[kernelfile name])

AC_ARG_WITH(mkubifs,
	[  --with-mkubifs=NAME mkubifs number [[628]]],
	[MKUBIFS_ARGS="$withval"],[MKUBIFS_ARGS=""])
AC_SUBST(MKUBIFS_ARGS)
AC_DEFINE_UNQUOTED(MKUBIFS_ARGS,"$MKUBIFS_ARGS",[mkubifs number])

AC_ARG_WITH(ubinize,
	[  --with-ubinize=NAME ubinize number [[628]]],
	[UBINIZE_ARGS="$withval"],[UBINIZE_ARGS=""])
AC_SUBST(UBINIZE_ARGS)
AC_DEFINE_UNQUOTED(UBINIZE_ARGS,"$UBINIZE_ARGS",[ubinize number])

AC_ARG_WITH(driverdate,
	[  --with-driverdate=NAME driver date [[628]]],
	[DRIVERDATE="$withval"],[DRIVERDATE=""])
AC_SUBST(DRIVERDATE)
AC_DEFINE_UNQUOTED(DRIVERDATE,"$DRIVERDATE",[driver date])

AC_ARG_WITH(rcidnum,
	[  --with-rcidnum=NUMBER rc id number [[2,...]]],
	[RCIDNUM="$withval"],[RCIDNUM=""])
AC_SUBST(RCIDNUM)
AC_DEFINE_UNQUOTED(RCIDNUM,"$RCIDNUM",[rc id number])

AC_ARG_WITH(debug,
	AS_HELP_STRING([--without-debug],[disable debugging code]),
	[with_debug="$withval"],[with_debug="yes"])
if test "$with_debug" = "yes"; then
	DEBUG_CFLAGS="-ggdb3"
	AC_DEFINE([DEBUG],[1],[Define to 1 to enable debugging code])
fi
AC_SUBST(DEBUG_CFLAGS)

AC_CONFIG_FILES([
Makefile
BoxBranding/Makefile
BoxBranding/lib/Makefile
])
AC_OUTPUT
