# coco-de-guide

Project plugin for the CoCo data engineering guide dbt project (DEMO_DB.TPCH_TRANSFORMED).

## Includes

- **Skills** (`skills/`)
  - `new-dbt-model` — creates a new dbt model using `source()` references, adds primary key tests to `_schema.yml`, and runs `dbt build`.
- **Agents** (`agents/`)
  - `dbt-review` — reviews changed dbt models against origin/main, runs `dbt build` on each, and reports PASS/FAIL per convention with remediation steps.
- **Hooks** (`hooks/hooks.json`)
  - `PreToolUse` on `bash` — `validate-bash.sh` blocks dbt commands that use `--target prod`; production changes go through CI/CD.
