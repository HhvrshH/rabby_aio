# RABBY AIO

Written by: @hvrsh (TG)

Channel: @hashvers (TG)

---

**BAS Automation for claiming points, referrals, and daily swaps**

**Setup on launch:**

1. Use Finger Switcher - whether to use fingerprints.
	1. Finger Print Key - if enabled **(1)**, enter the key to obtain fingerprints, available here - https://fingerprints.bablosoft.com/
3. Threads - number of concurrently running threads.
4. Work Mode - operating mode
	1. DBK -  to bridge assets to dbk and mint NFT's 
	2. Nothing - choose if you don't need to do anything with wallets but just check the Points Balance (Will work if `Try Claim Points - Yes`).
5. Chains - choose the chains on which you want to make a swap. (Do not select Celo, as there are no working routes for swapping). Swap only from the native token to the token.
6. Amount(From,To) - Range for bridge.
7. Count NFT mint - range from - to 
8. Gas - gas speed within Rabby. Be cautious to avoid long transaction times (affects the success of collecting points for the swap).
9. Sleep (in sec) - Sleep range. Do not set too low values, as claiming points occurs after sleep, and the claim button becomes available with a delay after the swap.
10. Gas Trigger - Gas trigger.
11. gasAPI - Can be left empty (if the trigger is not working correctly, obtain the key from etherscan).
12. Clear DoneList - After successful claiming or insufficient balance in all selected networks, private keys are recorded in the `done_list.txt` file. This helps the software understand which accounts it has passed and which ones it hasn't in case you interrupt its operation or the thread finishes with an error. If you need to run all wallets again (for example, a new day), choose Yes.

If you simply want to attempt to claim points, run `Try Claim Points - Yes` with `Work Mode - Nothing`.

**Setup on launch in `pointsChecker.xml`:**

1. Mode - 
	1. Snapshot points checker - the number of points at the time of the snapshot.
	2. Current points checker - the number of points at the current moment.

**Settings in files:**

`bal_checker_targets.json` - the minimum value to consider a balance insufficient in the network (you can leave it as default).

`invites.txt` - invitation codes, randomly selected.

`private.txt` - private keys.

`proxy.txt` - proxies, selected line by line.

`tokens_data.json` - lists of tokens that will participate in swaps.

`proxy_checker.txt` - proxies for the points checker, the more, the better.

`wallets.txt` - addresses to be checked by the checker.

---

**Автоматизация на БАСе для клейма поинтов, по рефкам, а также ежедневных свапов**

**Настройка при запуске `rabby_aio.xml`:**

1. Use Finger Switcher - использовать ли отпечатки.
	1. Finger Print Key - в случае включения **1** нужнно вести ключ для получения отпечатков, покупается тут - https://fingerprints.bablosoft.com/
3. Threads - количество потоков запущеных одновременно.
4. Work Mode  - режим работы
	1. DBK - бридж и минт нфт
	2. Nothing - выбираем если ничего делать не надо с кошельками, а просто чекнуть Баланс Поинтов (Сработает елси `Try Claim Points - Yes`).
5. Chains - выбор чейнов в которых в хотите сделать свап.(Celo не выбирать, нету рабочих маршрутов для свапа). Свап тольок с нативного токена в токен.
6. Amount(From,To) - Диапазон для бриджа.
7. Count NFT mint - диапазон соклько минтить нфт.
8. Gas - скорось газа внутри Rabby. Работать осторожно чтобы транза долго не висела (повлияет на успешность сбора поинтов за свап).
9. Sleep(in sec) - диапазон Сна. Нижние значение не ставить слишком малое, т.к клейм поинтов происходит после сна, а кнопка доступна для клейма с некой задержкой после свапа.
10. Gas Trigger - Ожидатель газа.
11. gasAPI - Можно оставлять пустым(если ожидатель работает некоректно то взять ключ в etherscan).
12. Clear DoneList - После успешного клейма или отсутствия достаточного баланаса во всех выбраных сетях в файл `done_list.txt` записываются приватники, чтобы софт понимал какие аккаунты он прошел а какие нет, в случае если вы прервали его работу или поток завершится с ошибкой. Если нужно прогнать все кошельки заново(новый день к примеру) - выбираем Yes.
 
 Если нужно просто попытатсья только заклеймить поинты, запустите  `Try Claim Points - Yes` с `Work Mode - Nothing`

 **Настройка при запуске `pointsChecker.xml`:**
 
 1. Mode - 
 	1. Snapshot points checker - количество поинтов на момент снапшота.
 	2. Current points checker -  количество поинтов на текущий момент.


 **Настройка в файлах**

 `bal_checker_targets.json` - меньше какого значения считать что не хватает баланса в сети (можно оставить по умлочанию) .

 `invites.txt` - инвайт коды, выбираются рандомно.

 `private.txt` - приватники.

 `proxy.txt` - прокси, выбираюся построчно.

 `tokens_data.json` - списки с токенами которые будут участвовать в свапах.

 `proxy_checker.txt` - прокси для чекера поинтов, чем больше тем лучше.

 `wallets.txt` - адреса для которые нужно проверить чеккером.
 
