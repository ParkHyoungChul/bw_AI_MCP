# MCP Client Setup (Windows PowerShell Version)

## 1️⃣ 프로젝트 생성 및 가상환경 설정

```powershell
# Create project directory
uv init mcp-client
cd mcp-client

# Create virtual environment
uv venv

# Activate virtual environment (Windows PowerShell)
.venv\Scripts\Activate.ps1
````

## 2️⃣ 필수 패키지 설치

```powershell
uv add google-generativeai mcp python-dotenv
```

## 3️⃣ 기본 파일 정리

```powershell
# Remove boilerplate files
Remove-Item .\main.py

# Create main file
ni .\client.py
```

(※ `ni`는 PowerShell의 `New-Item` 줄임말)

## 4️⃣ API Key 설정

```powershell
# Create .env file
ni .\.env
```

`.env` 파일을 열어 다음을 작성:

```env
GEMINI_API_KEY=<your key here>
```

## 5️⃣ .gitignore에 .env 추가

```powershell
echo ".env" >> .gitignore
```

