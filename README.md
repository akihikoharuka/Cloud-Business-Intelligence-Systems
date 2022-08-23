# Cloud-Business-Intelligence-Systems
The flow of data through the cloud, from its raw and ugly form to being visualised helping decision makers &amp; giving Business value.

might need VM(vm002)
1) Source: csv files saved on On premise machine under folder name: BI-System-Workshop-main
2) ETL : MS Data factory 
3) Sink : Azure SQL db name (sanjusrv/db001)
4) Storage account : adls for staging purpose(sanjustr001)

SQL queries:

create table dbo.Bajaj(Name varchar(100), rating varchar(50), purchase_type varchar(50) , state varchar(50))
create table dbo.Bosch(Name varchar(100), rating varchar(50), purchase_type varchar(50) , state varchar(50))
create table dbo.Philips_Viva(Name varchar(100), rating varchar(50), purchase_type varchar(50) , state varchar(50))
create table dbo.Philips_hl(Name varchar(100), rating varchar(50), purchase_type varchar(50) , state varchar(50))
create table dbo.preeti_blueleaf(Name varchar(100), rating varchar(50), purchase_type varchar(50) , state varchar(50))
create table dbo.preeti_zodiac(Name varchar(100), rating varchar(50), purchase_type varchar(50) , state varchar(50))
create table dbo.sujata(Name varchar(100), rating varchar(50), purchase_type varchar(50) , state varchar(50))

create table dbo.Bajaj(Name varchar(100), title varchar(100), rating varchar(100), purchase_type varchar(100), state varchar(100), view1 varchar(100), airbase varchar(100))
create table dbo.Bosch(Name varchar(100), title varchar(100), rating varchar(100), purchase_type varchar(100), state varchar(100), view1 varchar(100), airbase varchar(100))
create table dbo.Philips_Viva(Name varchar(100), title varchar(100), rating varchar(100), purchase_type varchar(100), state varchar(100), view1 varchar(100), airbase varchar(100))
create table dbo.Philips_hl(Name varchar(100), title varchar(100), rating varchar(100), purchase_type varchar(100), state varchar(100), view1 varchar(100), airbase varchar(100))
create table dbo.preeti_blueleaf(Name varchar(100), title varchar(100), rating varchar(100), purchase_type varchar(100), state varchar(100), view1 varchar(100), airbase varchar(100))
create table dbo.preeti_zodiac(Name varchar(100), title varchar(100), rating varchar(100), purchase_type varchar(100), state varchar(100), view1 varchar(100), airbase varchar(100))
create table dbo.sujata(Name varchar(100), title varchar(100), rating varchar(100), purchase_type varchar(100), state varchar(100), view1 varchar(100), airbase varchar(100))

{"type": "TabularTranslator","mappings": [
{"source": {"name": "Name","type": "String","physicalType": "String"},"sink": {"name": "Name","type": "varchar","physicalType": "varchar"}},
{"source": {"name": "Title","type": "String","physicalType": "String"},"sink": {"name": "title","type": "varchar","physicalType": "varchar"}},
{"source": {"name": "aiconalt","type": "String","physicalType": "String"},"sink": {"name": "rating","type": "varchar","physicalType": "varchar"}},
{"source": {"name": "View","type": "String","physicalType": "String"},"sink": {"name": "purchase_type","type": "varchar","physicalType": "varchar"}},
{"source": {"name": "State","type": "String","physicalType": "String"},"sink": {"name": "state","type": "varchar","physicalType": "varchar"}},
{"source": {"name": "View1","type": "String","physicalType": "String"},"sink": {"name": "view1","type": "varchar","physicalType": "varchar"}},
{"source": {"name": "asizebase","type": "String","physicalType": "String"},"sink": {"name": "airbase","type": "varchar","physicalType": "varchar"}}
]}

{"type": "TabularTranslator","mappings": [
{"source": {"name": "Name"},"sink": {"name": "Name"}},
{"source": {"name": "Title"},"sink": {"name": "title"}},
{"source": {"name": "aiconalt"},"sink": {"name": "rating"}},
{"source": {"name": "View"},"sink": {"name": "purchase_type"}},
{"source": {"name": "State"},"sink": {"name": "state"}},
{"source": {"name": "View1"},"sink": {"name": "view1"}},
{"source": {"name": "asizebase"},"sink": {"name": "airbase"}}
]}

drop table dbo.Bajaj
drop table dbo.Bosch
drop table dbo.Philips_Viva
drop table dbo.Philips_hl
drop table dbo.preeti_blueleaf
drop table dbo.preeti_zodiac
drop table dbo.sujata

