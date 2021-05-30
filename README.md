<b>PFILE</b> contains the Oracle parameters. This file is processed when an instance is started.

When an Oracle instance is started, the parameter file is searched for in $ORACLE_HOME/dbs (UNIX, Linux) or $ORACLE_HOME/database (Windows) in this order:

1) initSID.ora (PFILE)
2) PFILE (PFILE)

This is a basic PFILE for Oracle 12c on Windows:

*.audit_file_dest='<$ORACLE_BASE>\admin\<$ORACLE_SID>\adump'

*.audit_trail='none'

*.compatible='12.1.0'

*.control_files='<$ORACLE_BASE>\oradata\<$ORACLE_SID>\control01.ctl','<$ORACLE_BASE>\oradata\<$ORACLE_SID>\control02.ctl'

*.db_block_size=8192

*.db_domain=''

*.db_recovery_file_dest_size=5g

*.db_recovery_file_dest='<$ORACLE_BASE>\fast_recovery_area'

*.db_name='<$ORACLE_SID>'

*.diagnostic_dest='<$ORACLE_BASE>\diag'

*.dispatchers='(PROTOCOL=TCP) (SERVICE=<$ORACLE_SID>XDB)'

*.nls_language='ITALIAN'

*.nls_territory='ITALY'

*.open_cursors=300

*.pga_aggregate_target=200m

*.processes=300

*.remote_login_passwordfile='EXCLUSIVE'

*.sga_target=800m

*.undo_tablespace='UNDOTBS1'
