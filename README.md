
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B1020,45:14213D,100:2563EB&height=190&section=header&text=DevOps%20Journey&fontSize=46&fontColor=F8FAFC&fontAlignY=36&animation=fadeIn&desc=Learn%20by%20building%2C%20breaking%20and%20fixing&descAlignY=58&descSize=15" alt="DevOps Journey banner" width="100%" />

Привет! Я изучаю DevOps 🐧
Linux · Networking · Docker · Nginx · Git · CI/CD
Разбираюсь, как устроена инфраструктура, и закрепляю теорию практическими лабораторными.





</div>

👨‍💻 Обо мне
Я строю фундамент для старта в Junior DevOps / DevOps Internship. Предпочитаю не просто запоминать команды, а разбираться в механизмах: что делает система, почему возникает ошибка и как подтвердить, что исправление действительно сработало.
Мой подход к обучению:
Теория → лабораторная → наблюдение → troubleshooting → выводы
Сейчас основной фокус — Linux, компьютерные сети и практическая диагностика проблем.
🧰 Технологии и инструменты
<div align="center">

<img src="https://skillicons.dev/icons?i=linux,bash,docker,nginx,git,github,githubactions&perline=7" alt="Linux, Bash, Docker, Nginx, Git, GitHub and GitHub Actions icons" />

</div>

Linux и системное администрирование
- Процессы: PID/PPID, жизненный цикл процессов, сигналы, состояния процессов, ps, top, pstree, /proc.
- Права доступа: пользователи и группы, chmod, chown, права на файлы и каталоги.
- systemd: unit-файлы, .service, ExecStartPre, ExecStart, systemctl, journalctl, .slice.
- Ресурсы: основы cgroups v2, CPUQuota, MemoryMax, наблюдение за потреблением ресурсов.
- Изоляция: базовое понимание namespaces и их роли в контейнерах.
- Хранилище: файловые системы, inode, LVM (PV → VG → LV), расширение ext4/XFS.
- Диагностика: чтение логов, поиск причин отказов, проверка места на диске и потребления памяти.
Networking — изучаю и практикую
- IPv4, CIDR и подсети — изучаю основы и закрепляю вычисления.
- Шлюз и таблица маршрутизации: ip addr, ip route, ip route get.
- MAC, ARP и таблица соседей: ip neigh.
- DHCP, ICMP, DNS, NAT/PAT — разбираюсь в механизмах и проверяю их в лабораторках.
- TCP/UDP, порты и сокеты: ss, curl, ping, traceroute.
- Docker bridge networks, адреса контейнеров, маршруты и встроенный DNS.
Containers и web
- Docker: запуск контейнеров, пользовательские сети, подключение и отключение контейнеров, диагностика сетевой связности.
- Nginx: изучаю reverse proxy, upstream, порты и диагностику 502 Bad Gateway / Address already in use.
- Git: ветки, merge, rebase, fetch/pull, reset/revert, cherry-pick; изучаю командные workflow и PR-процесс.
- CI/CD: следующий этап — автоматизация проверок и сборок через GitHub Actions.
🧪 Практические лабораторные
Это учебные лабораторные и эксперименты. Я отмечаю текущий уровень честно и не выдаю их за production-опыт.

1. systemd Backup Service + Slice
Статус: ✅ собрана учебная версия
- Создан backup.service с Type=oneshot.
- Использованы ExecStartPre для подготовки каталога и ExecStart для запуска rsync.
- Сервис помещён в backup.slice для практики управления cgroup через systemd.
- Проверялись загрузка unit-файлов, запуск, статус и логи через systemctl и journalctl.
Что изучаю: управление жизненным циклом задач, разница между Unix-группами и systemd slices, диагностика ошибок сервиса.
2. Docker Networking Lab
Статус: 🧪 в процессе
- Создание пользовательской bridge-сети, например 172.19.0.0/16.
- Проверка адресов, шлюза и маршрутов контейнера с помощью ip addr и ip route.
- Исследование Docker DNS, ping, ARP/neighbor cache и доступности контейнеров.
- Отключение контейнера от сети и восстановление соединения для изучения отказов.
Что изучаю: как различать DNS, маршрутизацию, разрешение MAC-адресов и фактическую сетевую доступность.
3. Nginx Reverse Proxy Lab
Статус: 🛠️ в процессе
- Планирую направлять запросы с единого входного порта Nginx на два backend-приложения.
- Исследую listen, upstream, адреса и порты сервисов.
- Практикую расследование конфликтов портов через ss и проверку backend через curl.
Что изучаю: reverse proxy, разделение внешнего порта и портов приложений, диагностика Connection refused и 502 Bad Gateway.
4. Git Branching Practice
Статус: ✅ практика в учебном репозитории
- Работа с отдельными ветками testing/login, experiment и osnova.
- Создание merge-коммитов и чтение истории через git log --oneline --graph.
- Практика merge, rebase, fetch, pull, reset, revert и cherry-pick.
Следующий шаг: освоить Pull Request, code review, branch protection и базовый CI.
🔍 Как я подхожу к troubleshooting
1. Воспроизвожу симптом: что именно недоступно и как проявляется ошибка?
2. Собираю факты: статус сервиса, логи, порты, маршруты, ресурсы.
3. Формулирую гипотезы: не меняю несколько вещей одновременно.
4. Проверяю гипотезу: выбираю команду, которая подтверждает или опровергает её.
5. Исправляю и перепроверяю: проверяю не только статус, но и реальную работоспособность.
6. Записываю вывод: симптом → причина → решение.
🎯 Что изучаю дальше
- [ ] Уверенная IPv4-адресация: маски, CIDR и подсети.
- [ ] Маршрутизация, DNS, TCP/UDP, NAT и firewall в Linux.
- [ ] Nginx reverse proxy с двумя backend-приложениями.
- [ ] Bash-скрипты для автоматизации рутинных задач.
- [ ] GitHub Actions: тестирование и CI для учебного проекта.
- [ ] Больше практических инцидентов в Linux и Docker.
- [ ] Документировать лабораторные решения в отдельных репозиториях.
📚 Принцип, которым руководствуюсь
<div align="center">

Learn by doing.
Сначала понять механизм. Затем проверить руками. Потом сломать в лаборатории и восстановить.
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2563EB,55:14213D,100:0B1020&height=100&section=footer" alt="Blue footer banner" width="100%" />

</div>
