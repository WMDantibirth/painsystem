# painsystem
PainDatabase 文档
PANDATABASE是与疼痛相关的药物信息研究者的数据库系统。这个数据库整合了一些与疼痛相关的信息，药物，靶点，通路，疾病，副作用。药物和靶蛋白的基础数据来源于drugbank，副作用的基础数据来源于SIDER，通路和疾病，疾病的基础数据来源于KEGG。
相关技术
Python爬虫
Scrapy，Python开发的一个快速、高层次的屏幕抓取和web抓取框架，用于抓取web站点并从页面中提取结构化的数据。Scrapy用途广泛，可以用于数据挖掘、监测，自动测试。
Scrapy吸引人的地方在于它是一个框架，任何人都可以根据需求方便的修改。它也提供了多种类型爬虫的基类，如BaseSpider、sitemap爬虫等，最新版本又提供了web2.0爬虫的支持。
  Scrapy框架帮助编程者划分模块，预先编写多线程与反爬虫代码，使编程者专注于处理数据，学习门槛低。更重要的是，它集成了多种筛选数据和定位元素的方法，支持XPath和相对路径，可以方便准确地定位到具体的CSS元素，并且上述两种定位方式可以和传统正则表达式一起使用。在传统爬虫技术中，使用正则表达式抓取的数据往往不能完全符合预期要求，还需要编写大量的额外逻辑来处理文本，而使用xpath再配合正则表达式，在绝大部分情况下，都能准确定位到预期文本，使得爬取数据容易了很多。
Scrapy框架帮助编程者划分模块，预先编写多线程与反爬虫代码，使编程者专注于处理数据，学习门槛低。更重要的是，它集成了多种筛选数据和定位元素的方法，支持XPath和相对路径，可以方便准确地定位到具体的CSS元素，并且上述两种定位方式可以和传统正则表达式一起使用。在传统爬虫技术中，使用正则表达式抓取的数据往往不能完全符合预期要求，还需要编写大量的额外逻辑来处理文本，而使用xpath再配合正则表达式，在绝大部分情况下，都能准确定位到预期文本，使得爬取数据容易了很多。
MySQL数据库
MySQL是一个快速、支持多线程与多用户的关系型数据库服务器。作为一个开源的数据库，MySQL受到了广大开发者的喜爱，用户越多也就意味着这个开源数据库会越来越稳定、越来越高效。并且，MySQL在多线程编程和系统兼容性的表现上已经十分优秀，也可以轻松地支持上千万条记录，稳定性足以应付一个超大规模的数据库。在查询方面，MySQL支持查询SELECT和WHERE语句的全部运算符和函数，并且可以在同一查询中混用来自不同数据库的表。总而言之，对于本项目来说，MySQL完全能满足项目的需求，所以最终选定MySQL作为本项目的数据库服务器。
Flask框架
Flask是一个基于python的，微型web框架。之所以被称为微型是因为其核心非常简单，同时具有很强的扩展能力。它几乎不给使用者做任何技术决定。
　　安装flask时应该注意其必须的几个支持包比如Jinja2，Werkzeug等。如果使用easy_install或者pip这样的安装工具的话那么就不必担心这么多了。另外flask还有一些可选的辅助模块，使用它们可以让程序更加简洁易懂，比如SQLAlchemy用于数据库的连接和操作，flask-WTForm用于网页上表单的设计。
Bootstrap 和javascript
Bootstrap是Twitter推出的一个用于前端开发的开源工具包，提供了丰富的CSS样式、组件以及JavaScript框架，在Web开发者中颇受欢迎。Bootstrap具有简洁的风格，使用起来也十分灵活，具有响应式布局，使得Web开发者从痛苦的CSS样式开发中解脱出来。当一个团队没有设计师时，使用Bootstrap可以让开发者不必花费太多力气在前端样式上就可以编写出一个不至于太糟糕的页面，使得web开发更迅速，更简单。
  JavaScript(Java脚本)是一种基于对象（Object）和事件驱动（ Event Driven）并具有安全性能的脚本语言，使用JavaScript可以轻松的实现与HTML的互操作，并且完成丰富的页面交互效果，它是通过嵌入或调入在标准的HTML语言中实现的，它的出现弥补了HTML的缺陷，是java与HTML折衷的选择。
Beautifulsoup
简单来说，Beautiful Soup是python的一个库，最主要的功能是从网页抓取数据。官方解释如下：
Beautiful Soup提供一些简单的、python式的函数用来处理导航、搜索、修改分析树等功能。它是一个工具箱，通过解析文档为用户提供需要抓取的数据，因为简单，所以不需要多少代码就可以写出一个完整的应用程序。
Beautiful Soup自动将输入文档转换为Unicode编码，输出文档转换为utf-8编码。你不需要考虑编码方式，除非文档没有指定一个编码方式，这时，Beautiful Soup就不能自动识别编码方式了。然后，你仅仅需要说明一下原始编码方式就可以了。
Beautiful Soup已成为和lxml、html6lib一样出色的python解释器，为用户灵活地提供不同的解析策略或强劲的速度。
表信息
Mysql 数据库的E-R 图下图所示：
 

每个表的数据量大小

表名字	含义	数据条数
drugbank	Drugbank 药物信息表	85
drugbank_keggdrug	Drugbank和KEGG drug药物联系表	49
drugbank_target	Drugbak数据库中药物靶标信息表	268
Sider_effect 	SIDER 数据库中的药物副作用详细信息	602
sider_to_drug	SIDER数据库中药物副作用对应的药物	1381
Kegg_disease	Kegg Disease 数据库中的疾病信息表	10
pathway_table	Drugbank  数据库中的药物pathway	53
siderdrug_drugbank	Drugbank 数据库中药物id和SIDER药物id联系	684
kegg_disease_gene	Kegg disease  疾病和基因的对应关系	45
hpgdb_main	基因和对应的疼痛种类与相关资料	79
		
		
		
		
		
		


KEGG 表
CREATE TABLE kegg_drug(
kegg_id VARCHAR(200) PRIMARY KEY,
kegg_url VARCHAR(200),
Formula VARCHAR(200),
imgPath VARCHAR(200),
pic_kegg_structure VARCHAR(200),
Target_href VARCHAR(200),
Target_id VARCHAR(200),
Pathway_href VARCHAR(200),
Pathway_name VARCHAR(200),
img_pathway_path VARCHAR(200),
pic_kegg_pathway VARCHAR(200),
Structure_map_href VARCHAR(200),
Structure_map_name VARCHAR(200),
Structure_map_title VARCHAR(200),
img_Structure_path VARCHAR(200),
pic_kegg_structure_map VARCHAR(200)
);

Drugbank 表
create table drugbank(
drugbank_Name varchar(200) ,
drugbank_id varchar(200) primary key ,
drugbank_Type varchar(200) BINARY,
Groups varchar(200) BINARY,
Description text BINARY,
Structure varchar(200) BINARY,
CAS_number varchar(200) BINARY,
Weight varchar(200) BINARY,
has_Pathway_table varchar(200) BINARY,
has_target_table varchar(200) BINARY,
KEGG_Drug varchar(200) BINARY,
KEGG_Drug_link varchar(200) BINARY,
drugbank_url varchar(200)
);

Pathway表
create table pathway_table(
pathway_name varchar(200) primary key BINARY,
pathway_link varchar(200) BINARY,
drugbank_id varchar(200) BINARY
);


drugbank_target 表：
create table drugbank_target(
target_name varchar(200) primary key BINARY,
Kind varchar(200) BINARY,
Organism varchar(200) BINARY,
General_Function text ,
Specific_Function text(200) ,
Gene_Name varchar(200) BINARY,
Molecular_Weight varchar(200) BINARY,
drugbank_id varchar(200) BINARY,
Gene_sequence text
)

siderDrug_drugbank表：
create table siderDrug_drugbank(
drugbank_id varchar(200) primary key,
sider_drug_link varchar(200)
)

drugbank_keggDrug表
create table drugbank_keggDrug(
kegg_id varchar(200),
KEGG_Drug_link varchar(200),
drugbank_id varchar(200),
drugbank_url varchar(200)
);

sideeffect_of_sider_drug表
create table sideeffect_of_sider_drug(
sideeffect_link varchar(200) primary key,
sideeffect_name varchar(200),
sider_drug_name varchar(200),
sider_drug_link varchar(200)
);







sider_effect表

create table sider_effect(
sideeffect_link varchar(200) primary key ,
sideeffect_name varchar(200) ,
Definition text,
Synonyms text
);
sider_to_drug表
create table sider_to_drug(
drug_with_sideeffect_link varchar(200) primary key ,
drug_with_sideeffect varchar(200) ,
sideeffect_link varchar(200) 
);

kegg_drug_target表
create table kegg_drug_target(
Target_href varchar(200) primary key,
target_name varchar(200) ,
has_disease varchar(200) ,
has_pathway varchar(200) ,
target_id varchar(200) ,
Gene_name varchar(200) ,
Definition text,
aa_seq text,
nt_seq text
);


target_pathway表
create table target_pathway(
kegg_target_hsa varchar(200) primary key ,
kegg_target_hsa_link varchar(200) ,
kegg_target_pathway_name varchar(200) ,
pic_kegg_targets_pathway varchar(200) ,
Target_href varchar(200)
);





target_disease表
create table target_disease(
target_disease_link varchar(200) primary key ,
target_disease_id varchar(200) ,
target_disease_name varchar(200) ,
Target_href varchar(200) 
);

kegg_disease_gene表
create table kegg_disease_gene(
hsa_str varchar(200) primary key,
kegg_disease_link varchar(200),
kegg_id varchar(200)
);

kegg_disease表
create table kegg_disease(
kegg_disease_link varchar(200) primary key,
kegg_disease_id varchar(200),
kegg_disease_name varchar(200),
Description text,
Category varchar(200),
kegg_disease_pathway_id varchar(200),
kegg_disease_pathway_link varchar(200),
img_pathway varchar(200),
kegg_disease_pathway_name varchar(200)
);

hpgdb_main表
Loci	varchar(200) PK
Variants	varchar(200)
Alleles	varchar(200)
Phenotype	varchar(200)
Link	varchar(200)
Description	varchar(20000)
NUM	varchar(45)



设计思路
 总体思路：从drugbank找出治疗疼痛类药物的drugbank id，然后根据drugbank id 爬取drugbank的相关信息，其中有关联的kegg数据库的药物ID。根据再去爬取KEGG的药物相关信息。
PainDatabase涉及药物的多方面信息。药物的相关信息如：副作用、ATC、靶蛋白等。本项目将整合DrugBank、KEGG、Sider和的信息，具体如下：
药物的基本信息：药物名称、药物类型、药物所属的分类、药物描述、药物的结构图来自DrugBank。
副作用信息来自Sider。
通路的基本信息：通路名称、通路的描述、通路的结构图来自KEGG。
靶蛋白的基本信息：靶蛋白名称、靶蛋白的生物体、靶蛋白的药理作用等信息来自DrugBank。
药物与副作用的对应关系来自PubChem。
药物与通路的对应关系来自KEGG。
药物与靶蛋白的对应关系来自DrugBank。
基因与疼痛的对应关系来自GEEN
具体的实体联系集合在上面的E-R图显示出来。前段框架用了bootstrap,后端用了flask 。将数据库展示出来。
