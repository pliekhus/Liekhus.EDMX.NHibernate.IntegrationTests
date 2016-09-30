# Liekhus.EDMX.NHibernate.IntegrationTests
Generates integration tests based on the EDMX file

# Usage
The unit tests are generated into a partial class.  To add the rest you will need to add OneTimeSetup to wire your Interface to your Implementation to complete the integration test.

```c#
public partial class IDomainReportingNHibernateIntegrationTests
{
    [OneTimeSetUp]
		public void Configure()
		{
			DependencyHelper.Configure(new INinjectModule[] { new DomainNHibernateNinjectModule() });
		}
}
```
