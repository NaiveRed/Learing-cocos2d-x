
cocos2d-x learning journal
=========================
**NOTE**:�o�u�O�ھǲ�Cocos2d-x���������K�Ǿ�Markdown�A�j�h�O�ۤv���z�ѩM���O�A�]�����T�ʤ����O�ҡA�����W����n���оǺ���!�p�G���e�����ٷнЧi���C

�귽 : [API���](http://www.cocos2d-x.org/reference/native-cpp/V3.2alpha0/index.html)�B[�x�����](http://www.cocos2d-x.org/docs/README)
- - -

1. [���ҷǳ�](#environment)
2. [�M�׳Ы�](#creatNew)
3. [Hello World](#helloWorld)
4. [�֤߷���](#coreClasses)
5. [�p�ɾ�](#scheduler)
6. [��m](#position)
7. [�y�Шt](#coordinates)
8. [Log](#log)
9. [�r��](#string)
10. [����](#label)
11. [���](#menu)
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

OpenGL �M UI �y�Ф]���ഫ�� function�C

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
   
<h2 id="log">Log</h2>
[vsLog]:resource/logPosition.jpg
�i�H�bdebug���ɭԨϥΡA����K���A���ӬO�i�H��X��console�W�A���L�٤���o��ΡC

`log("%s update %d ",__TIME__, num++);`

��X���G:

![vs-log][vsLog]

<h2 id="string">�r��</h2>

���FC���ϥΪ�`char *` �M C++ ��`std::string`�A�bcocos2d-x���٦��@��`cocos2d-x::__String`�C

���]�ϥ�`std::string *str`�N�n�f�tnew�ӨϥΡA���ϥήɶ�delete(�άO�Q��smart pointer)�C

cocos2d-x::__String�i�H�Q��`create`�M`createWithFormat`�A
�h���κ޲z�O���骺����Ae.g.

	__String *str1(__String::create("HelloWorld!"));
	__String *str2(__String::createWithFormat("%d %s",123,"HelloWorld"));
	
�Ӧb�o�T�ئr�ꤤ�]�������ഫ��function�A�N���A�Բӻ����F�C

<h2 id="label">����</h2>

�b�C�����p�n��ܤ�r�i�H�Q�μ��ҡA�]�N�OLabel�A���O[HelloWorld](#helloWorld)�����Ϥ����A�W��@��HelloWorld�C

�bcocos2d-x 2����LabelTTF,LabelAtlas,LabelBMFont�T��class�A�o�̤���cocos2d-x 3.x���s��class Label�C

* **�t�έ�ͦr��**

		Label* Label::createWithSystemFont(
		const std::string& text,                                    //�r�ꤺ�e
		const std::string& font, 									//�r��
		float fontSize, 											//�r��j�p				
		const Size& dimensions /* = Size::ZERO */,  				//Label�b�ù��W�����j�p
		TextHAlignment hAlignment /* = TextHAlignment::LEFT */, 	//��������覡
		TextVAlignment vAlignment /* = TextVAlignment::TOP */		//��������覡
		)
		
* **TTF**

	���`�Ы�:

		Label* Label::createWithTTF(
		const std::string& text, 
		const std::string& fontFile, 								//�r���ɮ�(*.ttf)
		float fontSize, 
		const Size& dimensions /* = Size::ZERO */, 
		TextHAlignment hAlignment /* = TextHAlignment::LEFT */, 
		TextVAlignment vAlignment /* = TextVAlignment::TOP */
		)

	�ϥ�TTFConfig:
		
		Label* Label::createWithTTF(
		const TTFConfig& ttfConfig, 								//TTFConfig		
		const std::string& text, 
		TextHAlignment alignment /* = TextHAlignment::CENTER */, 	
		int maxLineWidth /* = 0 */									//�̤j��e�A�i�Ψӳ]�w�۰ʴ���
		)

	TTFConfig:
		
		typedef struct _ttfConfig
		{
		std::string fontFilePath;									//�r���ɮ�
		int fontSize;											

		GlyphCollection glyphs;										//�r���w(�r�Ŷ�)
		const char *customGlyphs;									//�ۭq�r���w
		
		bool distanceFieldEnabled;									//�z�Ѭ� �r��O�_���
		int outlineSize;											//�r���y��

		_ttfConfig(const char* filePath = "",
		int size = 12, 
		const GlyphCollection& glyphCollection = GlyphCollection::DYNAMIC,
		const char *customGlyphCollection = nullptr,
		bool useDistanceField = false,
		int outline = 0)
		:
		fontFilePath(filePath),
		fontSize(size),
		glyphs(glyphCollection),
		customGlyphs(customGlyphCollection),
		distanceFieldEnabled(useDistanceField),
		outlineSize(outline)
		
		{
			if(outline > 0)
			{
				distanceFieldEnabled = false;
			}
		}
		}TTFConfig;
				
e.g.
	
	auto label1(Label::createWithTTF("HelloWorld!", "fonts/Marker Felt.ttf", 60));
	
	TTFConfig ttf("fonts/Marker Felt.ttf", 60);
	ttf.outlineSize = 4;
	auto label2(Label::createWithTTF(ttf, "HelloWorld!"));

���~�٦� **createWithCharMap** �M **createWithBMFont**  (�Բӥi�d�\document�ά�CCLabel.h��������)�C

createWithCharMap���r���귽�Ӧ�*.png(�٦���L��)�A�ٶ��]�w�C�Ӧr�����e���C

��createWithBMFont�h�O�ϥ�\*.fnt�A�n���K�[�n�r���ɮסA�]�t�@�ӹϤ����ɮ�(\*.png)�M�r���y���ɮ�(\*.fnt)�A�ɮצW�ٶ��ۦP�C

����Label���@�ǮĪG:

shadow(���v)�BGlow(�å�)�BOutLine(�y��)

p.s. OutLine �P Glow �����|�_�Ĭ�

e.g.:

	label->enableOutline(Color4B::RED, 4);								//�Ĥ@�ӰѼƬ��䪺�C��A�ĤG�Ӭ��j�p
	label->enableShadow(Color4B(91, 0, 174, 128), Size(3, -10));       	//�Ĥ@�ӰѼƬ��C��A�ĤG�Ӭ����v���۹��m(��ڧ��@���N�i�H���դF)
	label->enableGlow(Color3B::GREEN);									//�å������	

	label->disableEffect();												//�����ĪG

�o�̵y�L�ɥR�@�U�`�`�Ψ쪺Color3B,color4B�N�t�b���S���z���סARGBA�AA:255���������z��

Label�٦��\�h��function�i�ϥΨҦp`label->setTextColor(Color4B(255, 0, 0,128))`

�i�H�q[�o��](http://www.cocos2d-x.org/reference/native-cpp/V3.2alpha0/db/de4/classcocos2d_1_1_label.html)�o���h��T!


<h2 id="menu">���</h2>
[menuUml]:resource/menuUml.png

![menu][menuUml]

�����@�U�ثe���z��:

�uMenu �~�ӤF Layer�A�ӿ�椤�S�]�t�F��涵��(Node <- MenuItem)�A�ҥH�ާ@�W�A�n�� MenuItem �[�i Menu�AMenu �A�[�i ���`�I�C

�@�ӳ����]�t�h�Ӽh�A�Ӽh�W�S���\�h�F��(e.g. Sprite�BMenu�BLabel...) �A���ONode�A�M��o�̪����Y�j���O MenuItem �[�i Menu�AMenu �A�[�i Layer�C�v
		
[�x�����](http://www.cocos2d-x.org/docs/manual/framework/native/v3/menu/zh)�]�����СC

* **��r���:**

MenuItemFont�BMenuItemAtlasFont�BMenuItemLabel �̭����Ѽƥi�q�{���X���ѩ�[API���](http://www.cocos2d-x.org/reference/native-cpp/V3.2alpha0/index.html)�o���C

�|��²�檺�Ҥl:
	
	MenuItemFont* onItem = MenuItemFont::create("on", CC_CALLBACK_1(HelloWorld::menuItemcallBack1,this));
	//Menu *menu(Menu::create(onItem, NULL));//�O�oNULL!!
	//menu->setPosition(Vec2::ZERO);
	
	menu->addChild(onItem);
	this->addChild(menu,1);

�b�Ы�MenuItem�ɶ��]�w�I���o�ͪ��ơA�]�N�O�ѼƦC����callback function�A�b�o�̧Q��macro: `CC_CALLBACK_1` ������ �A`HelloWorld::menuItemcallBack1`�h�O�ҥΨ쪺function�A
��M�A�ڭ̻ݭn�bHelloWorld���g�@��menuItemcallBack1��function:
	
	void menuItemcallBack1(cocos2d::Ref* pSender)
	{
	//do something...
	}
	
�ܩ�CC\_CALLBACK\_1���ԲӥΪk�M��l(CC\_CALLBACK\_0 1 2 3)�ݤF�ܦh�����٬O�������A�q���O��ѼƼƶq�����A
�᭱�p�G�F�ѤF�A�����C

p.s �x����󤤨ϥΪ���k�OLambda�B�⦡�C

* **���F���**(Sprite)

���F��檺��涵�����O�OMenuItemSprite�A�䤤�٦��@�ӭl�����O��MenuItemImage(�Ϥ����)�C

�ϥ�MenuItemSprite�ɡA�n���إ߱��ϥΪ����F(e.g. `Sprite *normalSprite = Sprite::create("menu/normal.png")`)

e.g.

	MenuItemSprite * MenuItemSprite::create(
	Node *normalSprite,					//���إ��`�ɪ����F
	Node *selectedSprite,				//���سQ��ܮɪ����F
	Node *disabledSprite,				//���ظT�ήɪ����F�A�i�ٲ�
	const ccMenuCallback& callback		//callback 
	)
	
	//MenuItemImage�h�O�ιϤ��Ы�
	MenuItemImage * MenuItemImage::create(
	const std::string& normalImage,
	const std::string& selectedImage,
	const std::string& disabledImage
	)
	
* **�������**(Toggle)

�}����檺���O�O MenuItemToggle �A�i�H�i��h�ت��A�������C(�Ҧp:�n�����}��)

�䤤�@�ثإߤ覡:

	MenuItemToggle * MenuItemToggle::createWithCallback(
	const ccMenuCallback &callback				//���ާ@��callback 
	, MenuItem* item,							//�i�������MenuItem
	...
	)

	//�x���d��
	auto item6 = MenuItemToggle::createWithCallback(
	[&](Ref*){ log("Toggle touched!");},			//lambda expression �A �ڭ̤]�i�H��CC_CALLBACK_1�Ӱ�
	MenuItemFont::create("On"),						//MenuItem
    MenuItemFont::create("Off"),
	NULL
	);

�٦��@��Menu��function���ЩM�ĪG�i�H�q�x����󤤾ǲ�!
	
p.s ����@�ǥi�ܰѼ�(`void func(...);`)���Ϊk�i�H�A�ۦ�d�\�C