### SDK���

��SDK�ǻ���ThinkPHP���������չ�����ֻ����ThinkPHPƽ̨��ʹ�ã�ThinkPHP�汾Ҫ��2.0���ϣ���DEMO���õ��˿������ֲ㣬�������DEMO��ʹ��ThinkPHP3.1.2�汾��

### Ŀǰ֧�ֵ�ƽ̨
Ŀǰ���õ�¼ƽ̨Ϊ����ѶQQ����Ѷ΢��������΢��������΢������������360�����꣬Github��Google��MSN��

### �������ļ�

ThinkSDK/ThinkOauth.class.php    SDK���࣬��Ҫ����Oauth����֤������ƽ̨��SDK����Ҫ�̳д��ࡣ    
ThinkSDK/sdk/DoubanSDK.class.php ����SDK 

**************** ��Ŀ�ļ� ********************
/��ĿĿ¼/Lib/OauthAction.class.php 


ʹ�÷���
1������SDK����ThinkPHP��Ŀ�����ļ�����������Ϣ����Ѷ�����ף���������΢����Ҫ�Ǹ�����д�Ǹ����á�

/* ��Ѷ΢������ */
'SNS_SDK_TENCENT'=> array(
	'APP_KEY'    => '', //Ӧ��ע��ɹ������� app_key
	'APP_SECRET' => '', //Ӧ��ע��ɹ�������app_secret
	'CALLBACK'   => 'http://servername/index.php/Oauth/callback/sns_type/tencent', //Ӧ����Ȩ��Ļص���ַ�������ע��Ӧ��ʱ��дһ��
	'SUCCESS'    => 'complete', //�ɹ���ȡ��access_token����ת���ķ�������������ת�������Ȩ��ҳ�棩
),
		
/* ����΢������ */
'SNS_SDK_SINA' => array(
	'APP_KEY'     => '', //Ӧ��ע��ɹ������� app_key
	'APP_SECRET'  => '', //Ӧ��ע��ɹ�������app_secret
	'CALLBACK'    => 'http://servername/index.php/Oauth/callback/sns_type/sina', //Ӧ����Ȩ��Ļص���ַ�������ע��Ӧ��ʱ��дһ��
	'SUCCESS'     => 'complete', //�ɹ���ȡ��access_token����ת���ķ�������������ת�������Ȩ��ҳ�棩
),
		
/* ����΢������ */
'SNS_SDK_163' => array(
	'APP_KEY'     => '', //Ӧ��ע��ɹ������� Consumer Key
	'APP_SECRET'  => '', //Ӧ��ע��ɹ������� Consumer Secret
	'CALLBACK'    => 'http://servername/index.php/Oauth/callback/sns_type/163', //Ӧ����Ȩ��Ļص���ַ�������ע��Ӧ��ʱ��дһ��
	'SUCCESS'     => 'complete', //�ɹ���ȡ��access_token����ת���ķ�������������ת�������Ȩ��ҳ�棩
),

2����Ȩ��ַ U('Oauth/oauthCode', 'sns_type=tencent') 
   �����sns_type=tencent �е�tencentΪSNS���ͣ���Ѷ - tencent,���� - sina, ���� - 163
   �ɲο�ʾ�� IndexAction.class.php

3, ���ýӿڣ���Ȩ֮��Ϳ����������ýӿڣ����£�
   import('ORG.SNS_SDK.TencentWeiBo'); //����ӿ���
   $tencent = new TencentWeiBo(); //ʵ�����ӿڶ���
   $tencent->tShow(); //���ýӿ�

4���ӿ������淶
   ���нӿڷ���������ΪSNSƽ̨�ṩ�Ľӿ�����ȥ����/����������/�������ĸ��д�����£�
   �ӿ�����t/add                   ��Ӧ�ķ���Ϊ   tAdd()
   �ӿ�����statuses/home_timeline  ��Ӧ�ķ���Ϊ   statusesHome_timeline()
   ����ӿ���ο�SNS����ƽ̨

5���ӿڲ����淶
   �ṩ���ִ��ݲ����ķ�ʽ
   a��URL��ѯ�ַ�����a=xxx&b=xxx
   b�����鷽ʽ�� array(a=>'xxx',b=>'xxx')
   ����ӿڲ�����ο�SNS����ƽ̨
   ע����ƽ̨�������ݸ�ʽĬ��Ϊ json ���Բ����ݴ˲���
       ��Ѷ΢����Ҫ�����û�IP��ϵͳ�Ѿ��Զ����ݣ����ýӿ�ʱ���Բ��ô��ݴ˲���
       �����������������⣬����ֻҪ�ǿ���ƽ̨�涨�ı�ѡ������ΪSDK�����ı�ѡ����
 
   
����ĩ�ύ��ϸ�ĵ�������ƽ̨�����淶