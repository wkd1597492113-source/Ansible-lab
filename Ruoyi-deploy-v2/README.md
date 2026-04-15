# RuoYi-deploy-v2

将 `RuoYi-deploy-V1.yml` 拆分为 Ansible Role 的版本。

## 目录结构

- `deploy.yml`: 主 playbook 入口
- `roles/ruoyi_deploy/defaults/main.yml`: 默认变量
- `roles/ruoyi_deploy/tasks/main.yml`: 部署任务
- `roles/ruoyi_deploy/templates/*.j2`: systemd 服务模板

## 使用方式

在 `Ansible-lab` 目录执行：

```bash
ansible-playbook -i inventory Ruoyi-deploy-v2/deploy.yml
```

如需覆盖变量，可在 inventory/group_vars 或命令行 `-e` 中设置。
