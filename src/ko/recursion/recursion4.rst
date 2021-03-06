재귀 횟수 세기
=====================

리보그는 세는 방법을 알고 있다... 하지만,
세는 방법을 아직 보지는 못했고 한동안 그럴 것이다.
여기서 지금까지 학습한 파이썬을 일부 알고 있다면,
숫자 변수를 사용해서 리보그가 어떻게 셀 수 있는지 알고 있을 것이다;
하지만, 여러분에게 그렇게 하지 않도록 부탁한다.


**Tokens 5** 세상을 선택한다.
리보그가 서있는 곳에, 토큰을 하나 발견할 수 있다.
리보그가 토큰을 집어(``take()``) 다음 정사각형으로 이동하는지는(``move()``) 알고 있다.
더이상 어떤 토큰도 찾을 수 없는 정사각형에 도착할 때까지 토큰을 집고, 이동하는 두 단계를
리보그가 반복하도록 한다.
그리고 나서, 정사각형에서 모은 모든 토근을 정사각형 한 곳에 놓고, 다음 정사각형으로 이동한다.

정확하게 똑같은 프로그램이 **Tokens 6**에서도 동작해야만 된다.
**Tokens 6** 세상에는 토큰 갯수가 다르다.
그래서, 고정된 반복 횟수를 갖지 않기 때문에, ``repeat`` 명령어를 사용할 수 없다.

리보그가 호주머니에 무한히 많은 토큰을 갖고 출발한다:
그래서, 한 지점에 토큰 내려놓기를 언제 멈출지 알아낼 수 없어서 ``carries_object()`` 도 사용할 수 없다.

.. topic:: 직접 시도해 보기!

    재귀를 사용해서 해당 문제를 해결하는 해법을 작성한다.
    해법에 대한 개요가 다음에 나와 있다::

        def collect():
            # 무언가 수행한다.
            # 무언가 수행한다.
            if 특정_조건:
                # 무언가 수행한다.
            # 무언가 수행한다.

        collect()
        move()

.. hint::

    기본 반복 명령어는 ``take()`` 와 ``move()`` 가 되고, 조건으로 ``object_here()`` 함수를 생각해볼 수 있다.

    .. code-block:: py3

        def collect():
            take()
            move()
            if object_here():
                collect()
            put()

        collect()
        move()


.. topic:: 재귀 도전과제

    이전에 수행했던 모든 도전과제를 재검토한다.
    ``while`` 루프 대신에 재귀를 사용하는 새로운 해법으로 코드를 작성한다.
