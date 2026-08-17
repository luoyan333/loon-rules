# Loon / OpenClash 自用规则

- `direct.conf`：Loon 直连规则。
- `proxy.conf`：Loon 代理规则。
- `openclash/direct.yaml`：自动生成的 OpenClash 直连规则集。
- `openclash/proxy.yaml`：自动生成的 OpenClash 代理规则集。

OpenClash YAML 使用 `rule-providers` 的 `classical` 格式。规则集本身不绑定具体策略组，引用 `direct.yaml` 时指定 `DIRECT`，引用 `proxy.yaml` 时指定所需代理策略组。

修改两个 `.conf` 文件后，GitHub Actions 会自动去重并更新 OpenClash YAML。也可以在本地运行：

```bash
python3 scripts/generate_openclash.py
```
