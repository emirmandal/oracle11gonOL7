# oracle11gonOL7
oracle11g  on oracle linux 7.5

as root
yum install oracle-rdbms-server-11gR2-preinstall

as root
xhost +

as root
yum install xorg-x11-apps.x86_64

as root
yum install elfutils-libelf-devel

as oracle
./runInstaller -silent -force FROM_LOCATION=/opt/database/stage/products.xml oracle.install.option=INSTALL_DB_SWONLY UNIX_GROUP_NAME=oinstall INVENTORY_LOCATION=/u01/app/oraInventory ORACLE_HOME=/u01/app/oracle/product/11.2.0 ORACLE_HOME_NAME="OraDb11g_Home1" ORACLE_BASE=/u01/app/oracle oracle.install.db.InstallEdition=EE oracle.install.db.EEOptionsSelection=false oracle.install.db.isCustomInstall=false oracle.install.db.DBA_GROUP=oinstall oracle.install.db.OPER_GROUP=oinstall DECLINE_SECURITY_UPDATES=true
