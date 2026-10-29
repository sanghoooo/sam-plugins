# hoo-plugins

sanghoooo의 Claude Code 플러그인 마켓플레이스입니다.

## 설치

Claude Code에서 마켓플레이스를 추가하고 쓸 플러그인을 설치합니다.

```
/plugin marketplace add https://github.com/sanghoooo/hoo-plugins.git
/plugin install sam-ui@hoo-plugins
```

터미널에서는 `claude plugin marketplace add https://github.com/sanghoooo/hoo-plugins.git` 후
`claude plugin install sam-ui@hoo-plugins`입니다. 한 프로젝트에서 팀이 함께 쓰려면 프로젝트 폴더에서 두 명령에
`--scope project`를 붙여 `.claude/settings.json`에 기록합니다.

업데이트는 `/plugin marketplace update hoo-plugins` 후 `/reload-plugins`입니다.

## 플러그인

| 플러그인 | 설명 | 소스 |
| --- | --- | --- |
| `sam-ui` | SAM UI Kit: React + Tailwind CSS 4 대시보드 킷을 프로젝트에 설치하고 그 킷으로 화면을 만듭니다. | [sanghoooo/sam-ui](https://github.com/sanghoooo/sam-ui)의 `plugins/sam-ui` |

각 플러그인의 라이선스는 그 소스 저장소를 따릅니다.

## 플러그인 추가

`.claude-plugin/marketplace.json`의 `plugins`에 항목을 더하고 README의 표에도 적습니다.

- **자기 저장소가 있는 플러그인**(앱 · 테스트 · 릴리스가 따로 있는 것): `git-subdir` 소스로 그 저장소의 플러그인
  폴더를 가리킵니다. 그 저장소의 기본 브랜치를 따라가므로, 그쪽에서 `plugin.json`의 버전을 올려 push하면 여기는
  고치지 않아도 업데이트가 갑니다.
- **작은 플러그인**(스킬 · 명령 몇 개): 이 저장소의 `plugins/<이름>/`에 두고 `"source": "./plugins/<이름>"`으로
  등록합니다.

고친 뒤 `claude plugin validate .`로 확인합니다.
