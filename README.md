## 1��SDK���

��SDK�ǻ���ThinkPHP���������չ�����ֻ����ThinkPHPƽ̨��ʹ�ã�ThinkPHP�汾Ҫ��2.0���ϣ���DEMO���õ��˿������ֲ㣬�������DEMO��ʹ��ThinkPHP3.1.2�汾��

## 2��Ŀǰ֧�ֵ�ƽ̨
Ŀǰ���õ�¼ƽ̨Ϊ����ѶQQ����Ѷ΢��������΢��������΢������������360�����꣬Github��Google��MSN��

## 3���������ļ�

ThinkSDK/ThinkOauth.class.php    SDK���࣬��Ҫ����Oauth����֤������ƽ̨��SDK����Ҫ�̳д���    
ThinkSDK/sdk/DoubanSDK.class.php ������SDK��    
ThinkSDK/sdk/GithubSDK.class.php ��Github SDK��    
ThinkSDK/sdk/GoogleSDK.class.php ��Google SDK��    
ThinkSDK/sdk/MsnSDK.class.php ��MSN SDK��    
ThinkSDK/sdk/QqSDK.class.php ����ѶQQ SDK��    
ThinkSDK/sdk/RenrenSDK.class.php ��������SDK��    
ThinkSDK/sdk/SinaSDK.class.php ������΢��SDK��    
ThinkSDK/sdk/T163SDK.class.php ������΢��SDK��    
ThinkSDK/sdk/TencentSDK.class.php ����Ѷ΢��SDK��    
ThinkSDK/sdk/X360SDK.class.php ��360 SDK��

## 4�����ø�ʽ

SDK�����ø�ʽ���£��ɲο�DEMO�е����ã�

	//��һ��(TYPE)�������Ӧ��SDK����
	'THINK_SDK_(TYPE)' => array(
		'APP_KEY'    => '', //Ӧ��ע��ɹ������� APP ID
		'APP_SECRET' => '', //Ӧ��ע��ɹ�������KEY
		'CALLBACK'   => '', //ע��Ӧ����д��callback
	)

## 5��ʹ�÷���

a�����ThinkPHP��չ��������ThinkSDKĿ¼���뵽ThinkPHP����չĿ¼��~Extend/Library/ORG/~��    
b�����SDK���ã����������ø�ʽ����Ŀ��������Ӷ�Ӧ��SDK���á����ɲο�DEMO�е������ļ���    
c����ת����Ȩҳ�棬����SDK����~import("ORG.ThinkSDK.ThinkOauth");~����ȡSDKʵ��~$sns=ThinkOauth::getInstance($type)~����ת����Ȩҳ��~redirect($sns->getRequestCodeURL())~�����ɲο�DEMO�е�Index/login������