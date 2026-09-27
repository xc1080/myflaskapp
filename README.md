# Flask Jenkins CI/CD Demo

[![Python](https://img.shields.io/badge/Python-Flask-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jenkins](https://img.shields.io/badge/Jenkins-pipeline-D24939?logo=jenkins&logoColor=white)](https://www.jenkins.io/)
[![Tests](https://img.shields.io/badge/tests-pytest-0A9EDC?logo=pytest&logoColor=white)](https://pytest.org/)

一个用于练习 Flask、自动化测试和 Jenkins Pipeline 的最小项目。根路由返回 `Hello, CI/CD with Jenkins!`，流水线覆盖依赖安装、代码检查、测试、覆盖率报告、打包和部署阶段。

## 本地运行

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

访问 `http://localhost:5000`。

## 测试与检查

```bash
pytest --cov=app tests/
flake8 app.py tests/
```

## 项目结构

```text
├── app.py           # Flask 应用
├── tests/           # pytest 测试
├── requirements.txt # Python 依赖
└── Jenkinsfile      # Jenkins 声明式流水线
```

> `Jenkinsfile` 当前包含特定 Windows 环境的 Python 路径和示例仓库地址，迁移到其他机器时需要按实际环境调整。

