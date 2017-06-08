# RecyclerView
- 별 거 없음.

# retrofit
- 별 거 없음.

### 팁
- BuildConfig로 환경설정값 불러오기
	- local.propeties에 값을 넣어놓는다. ex) api_key="12345"
	- 프로젝트 build.gradle에서 아래와 같이 코딩합니다.
	```
	ext {
			Properties properties = new Properties()
			properties.load(project.rootProject.file('local.properties').newDataInputStream())
			flickrApiKey = properties.getProperty('flickrApiKey', "\"\"")
	}
	```
	- 빌드를 하면 BuildConfig.java에 FLICKR_API_KEY가 생성됩니다.
- kotlin-extension을 쓰자.
