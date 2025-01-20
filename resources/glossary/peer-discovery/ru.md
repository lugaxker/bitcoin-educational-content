---
term: ИССЛЕДОВАНИЕ ЛИЧНОСТИ

---
Процесс, в ходе которого узлы сети Биткойн соединяются с другими узлами для получения информации. Когда узел Bitcoin только запускается, у него нет информации о других узлах сети. Тем не менее, он должен установить соединение, чтобы синхронизироваться с блокчейном, в котором накоплено больше всего работы. Для обнаружения этих пиров используется несколько механизмов, в порядке приоритета:


- Узел начинает работу с обращения к своему локальному файлу `peers.dat`, в котором хранится информация об узлах, с которыми он ранее взаимодействовал. Если узел новый, этот файл будет пуст, и процесс перейдет к следующему шагу;
- При отсутствии информации в файле `peers.dat` (что нормально для только что запущенного узла) узел выполняет DNS-запросы к DNS-серверам. Эти серверы предоставляют список IP-адресов предположительно активных узлов для установления соединений. Адреса DNS seed жестко закодированы в коде Bitcoin Core. Этого шага обычно достаточно для завершения обнаружения пиров;
- Если DNS-семена не отвечают в течение 60 секунд, узел может обратиться к посевным узлам. Это публичные узлы Биткойна, перечисленные в статическом списке из почти тысячи записей, интегрированном непосредственно в исходный код Bitcoin Core. Новый узел будет использовать этот список для установления первого соединения с сетью и получения IP-адресов других узлов;
- В том маловероятном случае, если все предыдущие методы не сработают, у оператора узла всегда есть возможность вручную добавить IP-адреса узлов для установления первого соединения.