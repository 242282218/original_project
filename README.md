# original_project

用于复用的规则与工具快照（SSOT）。统一维护 `ai/ssot/` 与 `ai/rules/`，平台输出为生成物。

## 快速开始

```powershell
python scripts/ai_rules_manager.py sync --global
python scripts/ai_rules_manager.py check
```

## 测试（统一入口）

```powershell
python scripts/run_tests.py --suite fast
```

- 配置：`ai/test_config.yaml`
- 日志：`logs/test/`（summary/stdout/stderr/junit）
- 仅在 Dev Container / CI 内运行

## 目录说明

- `ai/ssot/`：规则与技能源（唯一事实源）
- `ai/rules/`：公共工程规则
- `.trae/` `.lingma/` `.agent/` `.codex/`：平台输出（禁止手改）
- `scripts/`：同步/校验/测试入口脚本
- `.devcontainer/`：本地容器开发环境
- `.github/workflows/`：CI 测试与校验
