1.���������
	1.1 ������Ŀ����Ŀ�����
		dom4j-1.6.1.jar
		jaxen-1.1-beta-6.jar
		commons-beanutils-1.8.0.jar
		commons-logging.jar
		jstl.jar
		standard.jar
		
	1.2 ��������İ���
		cn.itcast.domain
		cn.itcast.dao
		cn.itcast.dao.impl
		cn.itcast.service
		cn.itcast.service.impl
		cn.itcast.web.controller  
		cn.itcast.web.UI  (user interface)(��Ϊ�û��ṩ�û������servlet)
		cn.itcast.utils
		junit.test
		
		��web-inf\jspĿ¼������jspҳ��
		
	1.3 ����Ŀ¼���棬�������ڱ����û����ݵ�xml�ļ�(users.xml)
	
	
2������ʵ��user
	private String id;
	private String username;
	private String password;
	private String email;
	private Date birthday;
	
3������dao
	3.1  ����UserDaoXmlImpl
			public void add(User user)
			public User find(String username)
			public User find(String username,String password)
			
	3.2  ��ȡ�ӿ�
	
	3.3  ���������ࣺ XmlUtils 
	3.4  ����������


4������service(service ��web���ṩ���е�ҵ�����)
 	4.1  ����BusinessService
 			public void registerUser(User user) throws UserExistException
 			public User loginUser(String username,String password);
 			
 
 5������web��
 	5.1 ����ע��
 		5.1.1  дһ��RegisterUIServletΪ�û��ṩע�����,���յ���������register.jsp
 		5.1.2  дregister.jsp
 		5.1.3  register.jsp�ύ���󣬽���RegisterServlet����
 		5.1.4  дRegisterServlet
 				1.�������У�������RegisterFormbean 
 				2��дWebUtils�����࣬��װ�������ݵ�formbean��
 				3�����У��ʧ�����ص�register.jsp�������Դ�����Ϣ
 				4�����У��ͨ��������service�����ݿ���ע���û�
 				
 	5.2 ������½
 		5.2.1  	дһ��LoginUIServletΪ�û��ṩע�����,���յ���������login.jsp	
 		5.2.2  	login.jsp�ύ��LoginServlet�����½����
 				
 				
 				
���� day14_user����
1����������
2���������ݿ�ͱ�
	create database day14_user;
	use day14_user;
	create table users(
		id varchar(40) primary key,
		username varchar(40) unique not null,
		password varchar(40) not null,
		email varchar(100),
		birthday date
	);	
	
	
3��дһ���������ݿ��dao	



preparedStatement��statement������
1��preparedStatement��statement�ĺ���
2��preparedStatement���Է�ֹsqlע�������
3��preparedStatement�����Զ����������sql������Ԥ���룬�Լ��������ѹ��
		
		