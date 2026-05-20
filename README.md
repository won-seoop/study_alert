# Study Alert

macOS 전용 무음 팝업 알림 스케줄러입니다.

```bash
bin/study-alert on 8 15 50
```

위 명령은 매일 `08:50`, `09:50`, `10:50`, ..., `15:50`에 알림을 띄웁니다.
기본 문구는 `[{minute}] 쉬는시간입니다. 고생하셨어요.` 입니다.

문구를 직접 지정할 수도 있습니다.

```bash
bin/study-alert on 8 15 50 "[{minute}] 물 마시고 쉬세요."
```

문구 안의 `{minute}`는 알림이 뜨는 시점의 분으로 바뀝니다.

```bash
bin/study-alert off
```

등록된 알림을 한 번에 끕니다.

```bash
bin/study-alert status
```

현재 등록 상태를 확인합니다.

알림은 `launchd`로 등록되며, 화면 중앙에 뜨는 팝업은 20초 후 자동으로 닫힙니다.
plist 위치는 다음과 같습니다.

```text
~/Library/LaunchAgents/com.wonhyeonseob.studyalert.plist
```
