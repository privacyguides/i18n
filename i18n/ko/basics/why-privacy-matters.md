---
title: "프라이버시를 신경 써야 하는 이유"
icon: 'material/shield-account'
---

현대 사회에서는 디지털 데이터가 온갖 곳에서 남용되고 있습니다. 디지털 프라이버시의 중요성은 그 어느때보다 높아졌지만, 많은 사람들은 이제와서 자신이 할 수 있는 것은 없다고 생각하는 경향이 있습니다. 하지만 실제로는 그렇지 않습니다. ==Your privacy is up for grabs==, and you need to care about it. Privacy is about power, and it is so important that this power ends up in the right hands.

Privacy is ultimately about human information, and this is important because we know that human information confers power over human beings. If we care about our ability to be authentic, fulfilled, and free humans, we have to care about the rules that apply to information about us. So much of our modern society is structured around **information**. When you shop online, read the news, look something up, vote, seek directions, or really anything else, you are relying on information. If we live in an information society, our information matters, and therefore privacy matters.

## '프라이버시'란?

많은 사람들은 **프라이버시**, **보안**, **익명성**의 개념을 혼동하곤 합니다. 어떤 서비스가 익명성을 제공하지 않는다는 이유로 '프라이버시 친화적이지 않다'며 비판하는 사람도 많습니다. 본 웹사이트에서는 이 세 가지 개념을 모두 주제로 다루고 있지만, 각 개념의 차이를 정확히 알고 언제 어떤 것이 필요한지를 이해해야 합니다.

**프라이버시**
:

=='프라이버시'란, '여러분에 대한 정보를 여러분이 관리하고 통제할 수 있는 권리'를 의미합니다.== 예를 들어, 메신저에서 여러분의 프라이버시를 보호하는 방법은 메신저에 종단 간 암호화를 적용하여 주고받는 메시지를 여러분 자신과 상대방 이외에는 아무도 볼 수 없게 하는 것입니다.

**보안**
:

Security is the ability to trust the applications you use—that the parties involved are who they say they are—and keep those applications safe. In the context of browsing the web, for example, security can be provided by HTTPS certificates.

    Certificates prove you are talking directly to the website you're visiting, and keep attackers on your network from reading or modifying the data sent to or from the website.

**익명성**
:

Anonymity is the ability to act without a persistent identifier. 익명성을 보장하는 대표적인 수단으로는 [Tor](../tor.md)가 있습니다. Tor를 이용하면 자신의 IP 주소나 네트워크 연결망을 사용하지 않고 임의의 IP 주소로 인터넷을 탐색할 수 있습니다.

    **'가명'**도 익명과 유사한 개념이지만, 가명은 실제 신원과 연결점이 없는 영구 식별자를 사용한다는 것이 특징입니다. '온라인에서 누구나 나를 `@GamerGuy12`라는 이름으로 찾을 수 있지만, 내 본명을 아는 사람은 아무도 없는 것', 이것이 바로 가명입니다.

All of these concepts overlap, but it is possible to have any combination of these. The sweet spot for most people is when all three of these concepts overlap. However, it's tricker to achieve than many initially believe. Sometimes, you have to compromise on some of these, and that's okay too. This is where **threat modeling** comes into play, allowing you to make informed decisions about the [software and services](../tools.md) you use.

[:material-book-outline: 위협 모델링에 대해 자세히 알아보기](threat-modeling.md ""){.md-button}

## "프라이버시를 원하는 사람은 뒤가 구린 사람이다"

'프라이버시를 지켜야 합니다'라고 주장할 때 항상 튀어나오는 반박은 **"숨길 게 없다면 프라이버시를 신경 쓸 이유가 없다"**라는 주장입니다. 이는 프라이버시를 지키고자 하는 사람들을 반사회적인 사람이나 범죄자처럼 묘사하고, 마치 프라이버시 보호는 잘못된 행동인 것 같은 느낌을 만들어내는 위험한 오해입니다.

=='무언가를 숨기거나 감추는 것'과 '사생활 보호'를 혼동하면 안 됩니다.== 여러분이 화장실에서 뭘 하는지는 명백함에도 불구하고, 여러분은 항상 화장실 문을 닫아둡니다. 이는 여러분이 무언가를 감추고자 한 것이 아닌, 사생활을 보호하고자 한 것이죠. 우리는 개인 건강 정보나 성생활 등 자신에 대한 정보를 여기저기 퍼뜨리고 다니는 것을 싫어하지만, 이런 마음가짐이 규탄받지는 않습니다. 사생활, 즉 프라이버시를 지키고자 하는 것은 정당한 욕구이며, 우리가 사람답게 살기 위해서는 반드시 필요한 것입니다. 프라이버시란, 비밀을 감추는 것이 아닌, '자신의 정보에 대한 권리를 강화하는 것'입니다.

## 프라이버시는 결국 '통제'인가요?

(디지털) 프라이버시의 일반적인 정의는 '자신에 대한 정보를 자신이 관리하고 **통제**할 수 있는 권리'입니다. 따라서 프라이버시를 '통제'로 생각하게 되는 것은 자연스럽습니다. 실제로 저희는 이런 생각을 가지고 본 웹사이트를 오랫동안 운영해 왔습니다. It sounds nice, and it appeals to many people, but in practice it just doesn't work.

Take cookie consent forms, for example. You may encounter these dozens of times per day on the various websites you visit, with a nice array of checkboxes and sliders which allow you to "curate" your preferences to exactly fit your needs. In the end, we just hit the "I Agree" button, because we just want to read the article or make a purchase. Nobody wants to complete a personal privacy audit on every single website they visit. This is an exercise in [choice architecture](https://en.wikipedia.org/wiki/Choice_architecture), designed to make you take the easy route out instead of delving into a maze of configuration options that don't need to exist in the first place.

==Control over your privacy inside most apps is an illusion.== It's a shiny dashboard with all sorts of choices you can make about your data, but rarely the choices you're looking for, like "only use my data to help me." This type of control is meant to make you feel guilty about your choices, that you "had the choice" to make the apps you use more private, and you chose not to.

Privacy is something we need to have baked into the [software and services](../tools.md) we use by default, you can't bend most apps into being private on your own.

## 출처

- Neil Richards - [Why Privacy Matters](https://www.amazon.com/Why-Privacy-Matters-Neil-Richards/dp/0190939044) (2021)
- [The New Oil: Why Privacy & Security Matter](https://thenewoil.org/en/guides/prologue/why/)
- [GitHub - @Thorin-Oakenpants](https://github.com/privacytools/privacytools.io/issues/1760#issuecomment-597497298)
