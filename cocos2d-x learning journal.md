
cocos2d-x learning journal
=========================
**NOTE**:�o�u�O�ھǲ�cocos2d-x�����O���K�Ǿ�markdown�A�]�����T�ʤ����O�ҡA
�����W����n���оǺ���!

- - -

1. [���ҷǳ�](#environment)
2. [�M�׳Ы�](#creatNew)
3. [Hello World](#helloWorld)

- - -

<h2 id="environment">���ҷǳ�</h2>

���h[�x��](http://www.cocos2d-x.org/download)�U��cocos2d-x (�ڥΪ��Ov3.5)
�A�U�������Y��i�H�ݨ�̭����� **setup.py**�A�ݭn�h�U��python�ӧ����w��
�A����python[�x��](https://www.python.org/downloads/)�U���ŦX�A�q��������python2.7+(���T�w3.x���椣��)�A�w�˦n��h�]�w�t���ܼƩάOcommand cd��python����Ƨ��A���ۦw��cocos2d-x�A
�bcommand��J:

`python setup.py`  (�|�]�Asetup.py����m�Ӧ��t���A�i�Nsetup.py�����令�ɮ׸��|)

�L�{�|��  NDK_ROOT�BANDROID_SDK_ROOT�BANT_ROOT �o�T�ӬO��Android�������A�ȥB�L���L��Enter�N�n�A�����w�ˡA���]�|���A�]�m�ncocos2d-x���t���ܼơC

<h2 id="creatNew">�M�׳Ы�</h2>

�bcommand�W��Jcocos�i�H�ݨ�������O�A�{�b�A��J
`cocos new -h` (�ݳЫػ���)�A�̷ӻ����b�ୱ�Ф@�ӷs���M��:

`cocos new -l cpp -d C:\Users\User\Desktop MySimpleTest` 

���}��Ƨ��i�H�ݨ�
Win 32�BiOS�BAndroid�Bwin8 �M Linux 5�رM�ץ��x(�Բӻ����i�ۦ�j�M)

�ڭ̿�win32���M���Visual Studio 2013 �}�ұM���ɡC

<h2 id="helloWorld">Hello World</h2>
[gHelloWorld]: resource/HelloWorld.jpg
�b�M���ɤ��i�H�ݨ���
AppDelegate.* ���{�������Ұʪ�code�A�A��main�̨өI�srun() function
`Application::getInstance()->run()`

HelloWorldScene.cpp��
`bool HelloWorld::init()` ���ԲӪ���������
�A����build and run�Y�i�C

��X���G:
![��X���G][gHelloWorld]
    




