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
	1. Initiations - claim points on accounts, log in through one of the refs from the `invites.txt` file.
	2. DailySwapping - swap to a random network from the selected token in a random token from the `tokens_data.json` file. I chose the most popular types of stablecoins and wrapped tokens, but you can replace them with your own tokens or remove those you don't need. Claim points for the swap.
	3. Nothing - choose if you don't need to do anything with wallets but just check the Points Balance (Will work if `Check Points - Yes`).
5. Chains - choose the chains on which you want to make a swap. (Do not select Celo, as there are no working routes for swapping). Swap only from the native token to the token.
6. Amount(From,To) - Range for the swap (in the native token).
7. Gas - gas speed within Rabby. Be cautious to avoid long transaction times (affects the success of collecting points for the swap).
8. Sleep (in sec) - Sleep range. Do not set too low values, as claiming points occurs after sleep, and the claim button becomes available with a delay after the swap.
9. Gas Trigger - Gas trigger.
10. gasAPI - Can be left empty (if the trigger is not working correctly, obtain the key from etherscan).
11. Check Points - Check points on accounts.
12. Clear DoneList - After successful claiming or insufficient balance in all selected networks, private keys are recorded in the `done_list.txt` file. This helps the software understand which accounts it has passed and which ones it hasn't in case you interrupt its operation or the thread finishes with an error. If you need to run all wallets again (for example, a new day), choose Yes.

If you just want to attempt to claim points, run `Check Points - Yes` with `Work Mode - Nothing`.

**Settings in files:**

`bal_checker_targets.json` - the minimum value to consider a balance insufficient in the network (you can leave it as default).

`invites.txt` - invitation codes, randomly selected.

`private.txt` - private keys.

`proxy.txt` - proxies, selected line by line.

`tokens_data.json` - lists of tokens that will participate in swaps.

---

**Автоматизация на БАСе для клейма поинтов, по рефкам, а также ежедневных свапов**

**Настройка при запуске:**

1. Use Finger Switcher - использовать ли отпечатки.
	1. Finger Print Key - в случае включения **1** нужнно вести ключ для получения отпечатков, покупается тут - https://fingerprints.bablosoft.com/
3. Threads - количество потоков запущеных одновременно.
4. Work Mode  - режим работы
	1. Initiations - клейм поинтов на акканутах, вход по одной из рефок с файла `invites.txt`.
	2. DailySwaping - свап в рандомной сети из выбраных в рандомный токен с списка в файле `tokens_data.json`. Взял саме популярные типы стейблов и врапнутых токенов, но можете заменить на свои токены или удалить те которых вам не нужны. Клейм поинтов за свап.
	3. Nothing - выбираем если ничего делать не надо с кошельками, а просто чекнуть Баланс Поинтов (Сработает елси `Check Points - Yes`).
5. Chains - выбор чейнов в которых в хотите сделать свап.(Celo не выбирать, нету рабочих маршрутов для свапа). Свап тольок с нативного токена в токен.
6. Amount(From,To) - Диапазон для свапа(в нативном токене).
7. Gas - скорось газа внутри Rabby. Работать осторожно чтобы транза долго не висела (повлияет на успешность сбора поинтов за свап).
8. Sleep(in sec) - диапазон Сна. Нижние значение не ставить слишком малое, т.к клейм поинтов происходит после сна, а кнопка доступна для клейма с некой задержкой после свапа.
9. Gas Trigger - Ожидатель газа.
10. gasAPI - Можно оставлять пустым(если ожидатель работает некоректно то взять ключ в etherscan).
11. Check Points - Проверять ли поинты на акканутах.
12. Clear DoneList - После успешного клейма или отсутствия достаточного баланаса во всех выбраных сетях в файл `done_list.txt` записываются приватники, чтобы софт понимал какие аккаунты он прошел а какие нет, в случае если вы прервали его работу или поток завершится с ошибкой. Если нужно прогнать все кошельки заново(новый день к примеру) - выбираем Yes.
 
 Если нужно просто попытатсья заклеймить поинты, запустите  `Check Points - Yes` с `Work Mode - Nothing`

 **Настройка в файлах**

 `bal_checker_targets.json` - меньше какого значения считать что не хватает баланса в сети (можно оставить по умлочанию) .

 `invites.txt` - инвайт коды, выбираются рандомно.

 `private.txt` - приватники.

 `proxy.txt` - прокси, выбираюся построчно.

 `tokens_data.json` - списки с токенами которые будут участвовать в свапах.
 