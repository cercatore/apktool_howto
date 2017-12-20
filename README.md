"# apktool_howto"

qui spiega 
https://medium.com/@felipecsl/bypassing-certificate-pinning-on-android-for-fun-and-profit-1b0d14beab2b

comando per decompilare
  apktool d my_apk.apk

comando per ricompilare

apktool b <folder> -o apk 
  expl:
    -o apk    opzionale
    -api 12   compila api compliant <12>
    -c        copia originale manifest
    
adesso in build ci sono i file
    e in dist cè my_apk.apk


 come SIGNARE la file
 jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 
    -keystore 
    ~/.android/debug.keystore 
    -storepass android example.unaligned.apk androiddebugkey     <---

esempio:    
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1
    -keystore
    //users/andrina/.android/debug.keystore