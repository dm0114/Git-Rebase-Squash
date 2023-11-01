## 정리

### 서론
Squash Merge, Rebase Merge 공부 결과를 기록한다.
본론에 앞서, Git을 왜 사용하는 지 한 번 생각해보고 가자.
미래의 우리가 Git History를 참조하여 코드를 관리하기 위해서 깃 그래프 관리는 필요해보인다.
(사실 아직 공감이 가는 단계는 아님;)

그래서 우리의 GIT History 접근하기 용이하도록, 그래프를 가독성 있게 만들 필요가 있다.
그것을 가능하게 만들어줄 도구들이 Squash, Rebase 전략이다.

### Squash Merge
여러 개의 기능 단위의 커밋 기록이 있다고 가정해보자.
- feat: A-1
- feat: A-2
- feat: A-3

우리는 이 기능 단위들을 [Feature A] 라고 그룹으로 관리하고 싶어졌다.<br/>
이런 상황에서 Squash Merge를 활용하여 여러 개의 커밋을 ***하나의 커밋으로 그룹처럼*** 만들어 원하는 브랜치에 Merge할 수 있다.

### Rebase Merge
Rebase는 Merge 대상 브랜치를 복사한 후, 대상 브랜치 위로 이어 붙여 그래프를 ***한 줄로 관리***할 수 있다.<br/>
Push의 경우 여러 기능들을 한 줄로 관리하여 사용할 때 유용해보인다. 
- 예를 들면, 위의 예에서 [Feature A], [Feature B], [Feature C]로 Develop Branch를 관리해 두었다면, Main에 Rebase로 머지한다면 이 기록들을 Main에서도 잘 확인할 수 있을 것 같다.
- 또 다른 예로는, 파생 브랜치들을 하나의 브랜치로 관리하고 싶은 경우 유용할 수도 있을 것 같다.

Rebase는 pull을 받을 때 유용하게 사용할 수 있는데, Merge Pull이 아닌 Rebase Pull을 사용하여 깃 그래프를 보다 가독성 있게 관리할 수 있다.<br/>
[그림을 통해 확인해보자.](https://dev.to/tandrieu/tiny-tips-git-pull-rebase-1hbi)
