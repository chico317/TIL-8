# TIL-8 인프런 공공데이터로~
isnull 혹은 isna 를 통해 데이터가 비어있는지를 확인할 수 있습니다. 결측치는 True로 표시되는데, True == 1 이기 때문에 이 값을 다 더해주면 결측치의 수가 됩니다. False == 0 
axis 0:행, 1:열
groupby는 series 형태로 연산속도가 빠르다 /  피봇테이블은 dataframe 형태(aggfunc 자동으로 mean으로 계산)

# df.loc는 행을 기준으로 가져옴.
df[열이름]: 결과가 Pandas의 Series 형태로 반환
예시)
#0번째 행의 "상호명"을 가져옵니다.
#df.loc[0]['상호명']
df.loc[0,'상호명']

# df.iloc[:] 전체 데이터를 가져옵니다.
df.iloc[행, 열] 순으로 인덱스 번호를 지정합니다.
: 은 전체를 의미합니다.
시작인덱스:끝나는인덱스+1을 써줍니다.
예) 3:5 라면 3번째 인덱스 부터 4번째 인덱스까지 가져옵니다.
: 에서 앞이나 뒤 인덱스를 써주지 않으면 처음부터 혹은 끝까지를 의미합니다.
예) :5 => 처음부터 4번 인덱스까지 가져옵니다.
예) 5: => 5번 인덱스부터 끝까지 가져옵니다.
예) -5: => 뒤에서 5번째 부터 끝까지 가져옵니다.
예) :-5 => 처음부터 5번째 전까지 가져옵니다.

# 레티나 디스플레이로 폰트가 선명하게 표시되도록 합니다.
from IPython.display import set_matplotlib_formats
set_matplotlib_formats('retina')
 
# 시각화를 위한 한글 폰트 설정 & 마이너스 폰트설정
plt.rc('font', family='Malgun Gothic')
plt.rc('axes',unicode_minus =False)

# 폰트가 선명하게 보이도록 설정
from IPython.display import set_matplotlib_formats
set_matplotlib_formats('retina')

# 파일 불러올때 csv 쉼표가 아니라 '|'로 구분될때
sep='|'

# isnull() 을 사용하면 데이터의 결측치를 볼 수 있습니다.
# 결측치는 True로 값이 있다면 False로 표시되는데 True 는 1과 같기 때문에 
# True 값을 sum()을 사용해서 더하게 되면 합계를 볼 수 있습니다.
# mean()을 사용하면 결측치의 비율을 볼 수 있습니다.
#f: 포멧스트링
