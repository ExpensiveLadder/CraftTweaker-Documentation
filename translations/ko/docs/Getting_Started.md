# 스크립트로 시작하기

CraftTweaker uses a custom scripting Language called `ZenScript`, ZenScript is read from `.zs` files that are stored in the `<gamedir>/scripts` folder.

ZenScript는 "하향식" 스크립팅 언어입니다. 즉, `imports`는 파일의 가장 위에 위치해야 하고, `변수 선언`도 파일의 상단에 위치해야 하지만, 제약은 없고 어디에서나 `변수`를 정의 할 수 있습니다. 그러나, 선언이 이루어지기 전에 해당 `변수`는 액세스 할 수 없습니다.

## 소개

이제까지 모드팩을 만들면서 그냥 여러 모드들을 던져 넣고 통합시켰던 경험이 없습니까? 각 모드들은 상대적으로 독립적으로 개발되기 때문에 특정 모드와 비교했을 때 강력함 차이를 느낄 수도 있습니다. 또는 일부 아이템들에 대해서 더 괜찮은 제조법이 있다고 생각할 수 있겠죠. 또는 모드를 제거하지 않고 특정 아이템만 제거하고 싶은 경우도 있을 수 있습니다. 또는 일부 광석사전 항목이 너무 많거나 너무 적은 경우를 발견할 수도 있습니다. 이제는 MineWeaker를 이용한 하나의 지시로 모든 작업을 수행 할 수 있습니다.

바닐라 마인크래프트를 지원하기 위해 제공되는 핵심 기능 외에도 모드 통합 라이브러리는 모드와 함께 제공됩니다. 이에 바닐라 제조법뿐만 아니라 모드에서 제공하는 제조법 및 모드의 동작을 수정할 수 있습니다.

## 스크립트

Scripts are stored in `<minecraftdir>/scripts` and are loaded in the `PreInitialization` phase of Minecraft, unlike previous versions of CraftTweaker, Scripts cannot be reloaded, this is due to changes that Mojang have made in 1.12 and there is no workaround. 또한, 스크립트가 정상적으로 동작하려면 **서버와 클라이언트 양쪽에** 다 위치해야 합니다.

스크립트 파일은 확장자가 `.zs`이며 `.zip`으로 압축시켜도 읽을 수 있습니다.

### 첫 번째 스크립트 작성

시작은 `<minecraftdir>/scripts` 폴더에 `hello.zs`라는 아주 기본적인 파일을 만드는 것입니다.

`hello.zs` 파일에 다음 코드를 입력하세요.

```zenscript
print("Hello world!");
```

이제 마인크래프트를 로드하고 `crafttweaker.log`파일을 확인하세요.

`crafttweaker.log` 파일은 `<minecraftdir>`에 위치하며, 일반 텍스트 파일을 읽을 수 있는 모든 프로그램에서 읽을 수 있습니다.

스크립트 파일을 편집하려면 Notepad++ 혹은 Sunlime Text를 사용하는걸 권합니다. 그러나 다른 프로그램으로도 가능합니다.

### craftweaker.log 파일

`crafttweaker.log` 파일의 출력내용에는 다음과 같은 특정 구문을 사용합니다.

    [LOADERSTAGE][SIDE][TYPE] <message>
    

위이 구문을 이용한 예제의 출력은 다음과 같습니다.

    [PREINITIALIZATION][CLIENT][INFO] Hello world!
    

이 구문은 디버그 목적으로 사용되며 구문을 사용하지 않는 부분은 덤프 명령으로인한 메시지 출력 부분입니다. 이 덤프를 복사-붙혀넣기를 하여 이용하면 편합니다.

### 주석

주석은 스크립트 파일을 더 읽기 쉽고 이해하기 쉽게 만드는데 도움을 줍니다.

ZenScript는 다음과 같은 세 가지 유형의 주석을 지원합니다.

한 라인: `// 한 줄 주석입니다.`

또 다른 한 라인: `# 이것 또한 한줄 주석입니다.`

복수 라인:

    /* 이건
    복수 라인의
    주석입니다. */