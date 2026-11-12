# project1

Spring XML dependency injection example. Requires JDK 17 or newer, Maven, and a running MySQL server.

## Run

1. Create the `NTSPBMS716DB` database and `SPRING_CUSTOMER_INFO` table in MySQL. The MySQL DAO inserts `CNAME`, `CADDRS`, `BILLAMT`, `DISCOUNT`, and `FINALAMOUNT`; any ID column must be generated automatically or have a default.
2. Adjust the URL and username in `src/main/resources/com/nt/commons/Info.properties` for your local database.
3. Set the `DB_PASSWORD` environment variable to your MySQL password in your IDE's Run Configuration. Do not commit the password. On PowerShell use `$env:DB_PASSWORD = 'your-local-password'`; on bash use `export DB_PASSWORD='your-local-password'`.
4. Run `mvn clean package`, then refresh/reimport the Maven project in your IDE.
5. Run `com.nt.test.RealtimeDITest1` (or `RealtimeDITest`) as a Java application and enter the requested customer details.

Spring XML and properties are stored in `src/main/resources` so Maven copies them into the runtime classpath.

If a real database password was previously committed, change it in MySQL. Removing it from the current files does not remove it from Git history.
