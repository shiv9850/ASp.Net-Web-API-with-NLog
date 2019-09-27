# ASp.Net-Web-API-with-NLog

Sample Application With ASP.net web api and Nlog

1.Create a web api application
2.Install NLog config
		use command Install-Package NLog.Config in package manger console
3.Edit NLog.Config.xml 
		replace following targets and rules tag with following code
		
		<targets>
				<target name="logfile" xsi:type="File" fileName="file.txt" />
		</targets>

		<rules>
			<logger name="*" minlevel="Debug" writeTo="logfile" />
		</rules>
		
4.Create a controller and action for testing logging

5.create instance of loggen in controller
		private static readonly NLog.Logger Logger = NLog.LogManager.GetCurrentClassLogger();
6.Add logging by using sutable method of Logger

7.Invoke Api and see file.txt in your project folder will get created 