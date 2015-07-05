
cocos2d-x learning journal
=========================
**NOTE**:�o�u�O�ھǲ�Cocos2d-x�����O���K�Ǿ�Markdown�A�j�h�O�ۤv���z�ѡA�]�����T�ʤ����O�ҡA�p�G�����нЧi���A
�����W����n���оǺ���!

- - -

1. [���ҷǳ�](#environment)
2. [�M�׳Ы�](#creatNew)
3. [Hello World](#helloWorld)
4. [�֤߷���](#coreClasses)
5. [�p�ɾ�](#scheduler)
6. [��m](#position)
7. [�y�Шt](#coordinates)

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

<h2 id="coreClasses">�֤߷���</h2>

Cocos2d-x�ĥξ𪬵��c�Ӻ޲zScene,Layer,Sprite,Menu...������(Node)�A
�N���ԲӤ���Director,Scene,Layer...��class���[�c�M���O�ϤF�A�Բӥi�q[�o��](http://www.cocos2d-x.org/reference/native-cpp/V3.2alpha0/index.html)�d��!

<h2 id="scheduler">�p�ɾ�</h2>

�j�P�W�N�O�i�H��Sprite������Ӷi��Ƶ{

�i�H�z�LAccess����Tag `label->setTag(42)` `this->getChildByTag(42)`�A�M��ϥ�

`void scheduleUpdate(void)` �� `void schedule(SEL_SCHEDULE selector,float interval)` �Ӷi��C������s(�q��:��fps����)
�A�b���i���s�����󤤷s�W`update(float dt)` function�A�O�o���A�ϥαƵ{�ɻݭn����Ƶ{�A�i�I�s`unscheduleUpdate()`�N�O������s�W��update function�A
�p�G�O�n�����L���禡�i�H��unschedule��unscheduleAllSelectors����C

<h2 id="position">��m</h2>

���F�ϥؼЧ��Ǫ���m�b�Q�n����m�W�A�N���F���I(Anchor Point)�o�ӪF��A�i�H��@Node�Ψ�l�ͪ��󪺩w���I�A��Anchor Point�O�۹��position����ҡA
�p: `Vec2(0.5,0.5)` �N�O����H�������C

p.s �i�z�L������I�M�]�w��m�A�|��[�F�ѡC

<h2 id="coordinates">�y�Шt</h2>

[CartesianCoordinates]:resource/CartesianCoordinates.png

Cocos2d-x���y�Шt�αĥβåd���y�Шt����**�k��y�Шt��**�A���U�������I�A�V�k��x���A�V�W��y���Az�b���V�ù��~�C

�åd���y�Шt(����/�k��):

![�åd���y�Шt][CartesianCoordinates]

�H�U���дX�خy�Шt:

* **OpenGL �y��**

�ϥΥk��y�Шt�C(Cocos2d-x���h�ĥ�OpenGLø�s)

* **UI �y��**

�]�٬��̹��y�Шt�ΡA���I�b���W���A�V�k��x���A�V�U��y���A
�bĲ���ƥ�άY�ǮɭԷ|�Ψ�C

* **�@�ɮy�ЩM�۹�y��**

�]���ݨ�۹�y�ФS�s�����a�y�СB�ҫ��y�СA�j�P�W���z�ѬO�@�ɮy�Ь������m�A�Ӭ۹�y�Ыh�O�H�t�@Node���󬰰�ǡA
��̤��S�����O���O�HAnchorPoint����ǡA�ȧڻ{�������A�Բӥi�A�hgoogle�C

**�ഫ����k**

�o������F���֮ɶ��ݨҤl�M�z�ѡA���M�٦��I�����ҥH...
�����ΨҤl�ӻ���:

�x���Ҥl:

	Sprite *sprite1 = Sprite::create("CloseNormal.png");
	sprite1->setPosition(Vec2(20,40));
	sprite1->setAnchorPoint(Vec2(0,0));
	this->addChild(sprite1);

	Sprite *sprite2 = Sprite::create("CloseNormal.png");
	sprite2->setPosition(Vec2(-5,-20));
	sprite2->setAnchorPoint(Vec2(1,1));
	this->addChild(sprite2);

	Vec2 point1 = sprite1->convertToNodeSpace(sprite2->getPosition());
	Vec2 point2 = sprite1->convertToWorldSpace(sprite2->getPosition());
	Vec2 point3 = sprite1->convertToNodeSpaceAR(sprite2->getPosition());
	Vec2 point4 = sprite1->convertToWorldSpaceAR(sprite2->getPosition());

	log("position = (%f,%f)",point1.x,point1.y);
	log("position = (%f,%f)",point2.x,point2.y);
	log("position = (%f,%f)",point3.x,point3.y);
	log("position = (%f,%f)",point4.x,point4.y);
	
���G:
	
	position = (-25.000000,-60.000000)
	position = (15.000000,20.000000)
	position = (-25.000000,-60.000000)
	position = (15.000000,20.000000)
	
convertToNodeSpace: �N�@�ɮy���ର�۹�y�СA�ഫ�覡: **�Hsprite1�����U�������I**�A���s�p��s���y�СC

convertToWorldSpace: �Nsprite2����m�y���ର�@�ɮy�СA�ഫ�覡: sprite1����m���ܡA�@�ɮy�Ъ��y�жb�]���ܡA
**�Hsprite1�����U�����I�A�إߤ@�ӷs���y�Шt(���a�y��)�A�Nsprite2���]��m��s�ت��o�Ӯy�Шt(�y�Ф���)�A�M��H��Ӫ��@�ɮy�Ь��Ѧҭ��s�p��sprite2����m**�C

convertToNodeSpaceAR: �N�@�ɮy���ର�۹�y�СA�ഫ�覡: **�Hsprite1�����I�����I**�A���s�p��s���y�СC

convertToWorldSpaceAR: �Nsprite2����m�y���ର�@�ɮy�СA�ഫ�覡: sprite1����m���ܡA�@�ɮy�Ъ��y�жb�]���ܡA
**�Hsprite1�����I�A�إߤ@�ӷs���y�Шt(���a�y��)�A�Nsprite2���]��m��s�ت��o�Ӯy�Шt(�y�Ф���)�A�M��H��Ӫ��@�ɮy�Ь��Ѧҭ��s�p��sprite2����m**�C
   




