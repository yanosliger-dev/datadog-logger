Adds a log section for custom logs in datadog

vars required to run

log_file_path: *full path to the log file you want to add
log_file_ower: *owner or user with acess to the log
logger_name: *name you want the service to tag as in DD
adm_group_required: does the dd-agent need adding to the adm group to access these logs

defaults set to syslog


Usage

---
- hosts:
    - all
  become: yes
  roles:
    - role: yanosliger_dev.datadog_smartmon
  vars:
    - log_file_path: /var/log/syslog
    - log_file_owner: syslog
    - logger_name: customlog
    - adm_group_required: True/False
