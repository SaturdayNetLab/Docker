# Docker
Was ist Docker?

Docker ist eine Plattform zur Automatisierung der Bereitstellung und Verwaltung von Anwendungen in Containern. Container sind leichtgewichtige, isolierte Umgebungen, die eine Anwendung und alle ihre Abhängigkeiten beinhalten, sodass sie überall konsistent ausgeführt werden können. Docker vereinfacht die Bereitstellung von Software, da es sicherstellt, dass die Anwendung unabhängig von der zugrunde liegenden Infrastruktur und den Betriebssystemen reibungslos läuft.

Mit Docker kannst du Anwendungen in Containern verpacken, die unabhängig von ihrer Umgebung ausgeführt werden können. Dies hilft dabei, die Entwicklung und Bereitstellung von Software zu beschleunigen und zu vereinheitlichen.
Was sind die YAML-Dateien?

In diesem Repository befinden sich verschiedene YAML-Dateien, die für die Automatisierung und Verwaltung von Docker-Containern verwendet werden. Diese Dateien sind Playbooks, die in Kombination mit Ansible oder Docker Compose verwendet werden. Sie ermöglichen es, Docker-Container schnell zu konfigurieren und zu starten, sodass du deine Anwendungen in einer wiederholbaren und skalierbaren Weise ausführen kannst.
Beispiele für YAML-Dateien in diesem Repository:

    Docker Compose YAML-Dateien: Diese Dateien definieren mehrere Docker-Container und deren Netzwerke, Volumes und Konfigurationen. Sie ermöglichen es, komplexe Anwendungen mit mehreren Container-Diensten zu starten.
    Ansible Playbooks: Diese YAML-Dateien sind für die Automatisierung von Docker-Installationen und die Bereitstellung von Containern auf verschiedenen Hosts verantwortlich. Sie ermöglichen es dir, Docker und Container auf mehreren Maschinen zu verwalten und zu konfigurieren.

Verwendung

Um die YAML-Dateien zu verwenden, kannst du entweder Docker Compose oder Ansible verwenden, je nach Bedarf:

    Docker Compose:
        Verwende die docker-compose.yml, um mehrere Container zu definieren und mit einem einzigen Befehl zu starten.
        Beispiel: docker-compose up -d
