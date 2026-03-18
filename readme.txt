# langsmith-study
langsmith 학습용 repository입니다.
!pip install -U langchain langchain-openai

# 1. 랭스미스 추적 기능 켜기
os.environ["LANGCHAIN_TRACING_V2"] = "true"

# 2. 랭스미스 API 키 설정
os.environ["LANGCHAIN_API_KEY"] = "lsv2_pt_94cd11"
os.environ["OPENAI_API_KEY"] = "sk-proj-FGl"

# 3. 프로젝트 생성
os.environ["LANGCHAIN_PROJECT"] = "My_First_Agent"

from langchain.chat_models import init_chat_model

model = init_chat_model("gpt-5-nano")

response = model.invoke("랭스미스가 무엇인지 한 문장으로 설명해줘.")
print(f"답변: {response.content}")

