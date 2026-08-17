# Project AETHER Makefile
# 世界最高峰のアプリ開発を支援する

.PHONY: all install dev test lint format docs clean build release help

# デフォルトターゲット
all: help

# ヘルプ
help:
@echo "🌌 Project AETHER - Makefile Targets"
@echo "======================================"
@echo ""
@echo "インストール:"
@echo "  install     - 本番用依存関係をインストール"
@echo "  dev         - 開発用依存関係をインストール"
@echo "  pre-commit  - 事前コミットフックをインストール"
@echo ""
@echo "テスト・品質:"
@echo "  test        - 全テストを実行"
@echo "  test-cov    - テストとカバレッジレポート"
@echo "  lint        - リンティングを実行"
@echo "  format      - コードフォーマット"
@echo "  type-check  - 型チェックを実行"
@echo "  security    - セキュリティ監査"
@echo ""
@echo "ドキュメント:"
@echo "  docs        - ドキュメントをビルド"
@echo "  docs-serve  - ドキュメントサーバーを起動"
@echo ""
@echo "ビルド・リリース:"
@echo "  build       - パッケージをビルド"
@echo "  clean       - ビルド成果物をクリーン"
@echo "  release     - リリースを準備"
@echo ""
@echo "実行:"
@echo "  run         - アプリを実行"
@echo "  run-dev     - 開発モードで実行"
@echo ""
@echo "その他:"
@echo "  benchmark   - ベンチマークを実行"
@echo "  profile     - プロファイリングを実行"

# インストール
install:
@echo "📦 Installing production dependencies..."
pip install -r requirements.txt

dev:
@echo "🔧 Installing development dependencies..."
pip install -r requirements-dev.txt

pre-commit:
@echo "🪝 Installing pre-commit hooks..."
pre-commit install

# テスト
test:
@echo "🧪 Running tests..."
pytest

test-cov:
@echo "🧪 Running tests with coverage..."
pytest --cov=core --cov=crypto --cov=math --cov-report=html --cov-report=term-missing
@echo "📊 Coverage report generated at htmlcov/index.html"

# リンティング
lint:
@echo "🔍 Running linters..."
flake8 core crypto math
pylint core crypto math

format:
@echo "✨ Formatting code..."
black core crypto math
isort core crypto math

type-check:
@echo "🔤 Running type checker..."
mypy core crypto math

# セキュリティ
security:
@echo "🔒 Running security audit..."
bandit -r core crypto math
safety check
detect-secrets scan --baseline .secrets.baseline

# ドキュメント
docs:
@echo "📚 Building documentation..."
sphinx-build -b html docs/source docs/build
mkdocs build

docs-serve:
@echo "📖 Starting documentation server..."
mkdocs serve

# ビルド
build:
@echo "🏗️ Building package..."
python -m build

clean:
@echo "🧹 Cleaning build artifacts..."
rm -rf build/ dist/ *.egg-info
rm -rf __pycache__/ */__pycache__/
rm -rf .pytest_cache/ .coverage htmlcov/
rm -rf .mypy_cache/
find . -type d -name "*.egg" -exec rm -rf {} +
find . -type f -name "*.pyc" -delete
find . -type f -name "*.pyo" -delete
@echo "✅ Clean complete!"

# リリース
release: clean test lint type-check build
@echo "🚀 Preparing release..."
@echo "Version: $$(grep '^version =' pyproject.toml | cut -d'\"' -f2)"
@echo "✅ Release ready! Upload with: twine upload dist/*"

# 実行
run:
@echo "🚀 Starting AETHER Core..."
python3 core/aether_core.py

run-dev:
@echo "🔧 Starting AETHER Core in development mode..."
python3 -u core/aether_core.py

# ベンチマーク
benchmark:
@echo "⚡ Running benchmarks..."
pytest --benchmark-only

profile:
@echo "📊 Running profiler..."
py-spy record -o profile.svg -- python3 core/aether_core.py

# Docker
docker-build:
@echo "🐳 Building Docker image..."
docker build -t project-aether:latest .

docker-run:
@echo "🐳 Running Docker container..."
docker run -it --rm project-aether:latest

# CI/CD
ci: lint type-check test security
@echo "✅ CI checks passed!"

# バージョン表示
version:
@echo "🌌 Project AETHER Version: $$(grep '^version =' pyproject.toml | cut -d'\"' -f2)"

# 美しさチェック
beauty-check:
@echo "🎨 Checking beauty score..."
@python3 -c "from core.aether_core import AetherCore; ac = AetherCore(); print(f'Beauty Score: {ac.generate_beauty_optimization()}')"

# 滑らかさチェック
smoothness-check:
@echo "✨ Checking smoothness index..."
@python3 -c "from core.aether_core import AetherCore; ac = AetherCore(); status = ac.get_system_status(); print(f'Smoothness: {status[\"smoothness\"]}')"

# 量子耐性チェック
quantum-resistance-check:
@echo "🔐 Checking quantum resistance..."
@python3 -c "from core.aether_core import AetherCore; ac = AetherCore(); status = ac.get_system_status(); print(f'Quantum Resistance: {status[\"quantum_resistance\"]}')"

# 完全チェック
full-check: lint type-check test security beauty-check smoothness-check quantum-resistance-check
@echo "✅ All checks passed! System is OPTIMAL."
