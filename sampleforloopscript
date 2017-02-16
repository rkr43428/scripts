#!/bin/bash
echo "THIS IS BACKUP SCRIPT"

LOG_DIR='/home/devops/training/vagrant/vagrant_exercise2/bash/test1'
BACKUP_DIR='/home/devops/training/vagrant/vagrant_exercise2/bash/backuplogs'

mkdir -p $BACKUP_DIR

echo "backuplogs directory created"

for bkp  in $(cat /home/devops/training/vagrant/vagrant_exercise2/bash/backupscrpt.txt);
do
if [ -f $LOG_DIR/$bkp ]
then
echo
echo "copying $bkp to backuplogs Directory"
echo
cp $LOG_DIR/$bkp $BACKUP_DIR
else
echo
echo "$bkp log files does not esixts, SKIPPING"

fi
done
echo
echo
echo "ZIPING backup directory"
tar -zcvf backup_logs.tgz /home/devops/training/vagrant/vagrant_exercise2/bash/backuplogs

echo
echo
echo "BACKUP FINISHED SUCCESSFULLY"
echo
