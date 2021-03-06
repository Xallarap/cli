---

copyright:

  years: 2018


lastupdated: "2018-10-17"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:tip: .tip}

# Plug-in
{: #ibmcloud_commands_settings}

{{site.data.keyword.Bluemix}} unterstützt ein Plug-in-Framework zur Erweiterung der verfügbaren Funktionalität. Verwenden Sie die folgenden Befehle, um die Plug-ins der {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle zu verwalten.
{: shortdesc}

<table summary="ibmcloud-Befehle, die Sie zur Verwaltung der Plug-ins der {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle verwenden können.">
 <thead>
 </thead>
 <tbody>
<tr>
  <td>[ibmcloud plugin repo-add](cli_plugin.html#ibmcloud_plugin_repo_add)</td>
  <td>[ibmcloud plugin repo-remove](cli_plugin.html#ibmcloud_plugin_repo_remove)</td>
  <td>[ibmcloud plugin repo-plugins](cli_plugin.html#ibmcloud_plugin_repo_plugins)</td>
  <td>[ibmcloud plugin repo-plugin](cli_plugin.html#ibmcloud_plugin_repo_plugin)</td>
  <td>[ibmcloud plugin list](cli_plugin.html#ibmcloud_plugin_list)</td>
</tr>
<tr>
  <td>[ibmcloud plugin show](cli_plugin.html#ibmcloud_plugin_show)</td>
  <td>[ibmcloud plugin install](cli_plugin.html#ibmcloud_plugin_install)</td>
  <td>[ibmcloud plugin uninstall](cli_plugin.html#ibmcloud_plugin_uninstall)</td>
  <td>[ibmcloud plugin update](cli_plugin.html#ibmcloud_plugin_update)</td>
  <td>[ibmcloud plugin repos](cli_plugin.html#ibmcloud_plugin_repos)</td>
</tr>
 </tbody>
 </table>


 ## ibmcloud plugin repos
{: #ibmcloud_plugin_repos}

Alle Plug-in-Repositorys auflisten, die in der Befehlszeilenschnittstelle von {{site.data.keyword.Bluemix_notm}} registriert sind.

```
ibmcloud plugin repos
```

<strong>Voraussetzungen</strong>: Keine

## ibmcloud plugin repo-add
{: #ibmcloud_plugin_repo_add}

Neues Plug-in-Repository zur Befehlszeilenschnittstelle von {{site.data.keyword.Bluemix_notm}} hinzufügen.

```
ibmcloud plugin repo-add REPO_NAME REPO_URL
```

<strong>Voraussetzungen</strong>: Keine

<strong>Befehlsoptionen</strong>:

   <dl>
   <dt>REPO_NAME (erforderlich)</dt>
   <dd>Der Name des Repositorys, das hinzugefügt werden soll. Sie können einen eigenen Namen für jedes Repository definieren.</dd>
   <dt>REPO_URL (erforderlich)</dt>
   <dd>Die URL des Repositorys, das hinzugefügt werden soll. Die URL des Repositorys muss das Protokoll (zum Beispiel 'http://plugins.ng.bluemix.net' anstatt 'plugins.ng.bluemix.net') enthalten. http://plugins.ng.bluemix.net ist das offizielle Plug-in-Repository der {{site.data.keyword.Bluemix_notm}}-CLI.</dd>
    </dl>


<strong>Beispiele</strong>:

Offizielles Plug-in-Repository der {{site.data.keyword.Bluemix_notm}}-CLI als `IBM Cloud-repo` hinzufügen:

```
ibmcloud plugin repo-add IBM Cloud-repo http://plugins.ng.bluemix.net
```

## ibmcloud plugin repo-remove
{: #ibmcloud_plugin_repo_remove}

Plug-in-Repository aus der {{site.data.keyword.Bluemix_notm}}-CLI entfernen.

```
ibmcloud plugin repo-remove REPO_NAME
```

<strong>Voraussetzungen</strong>: Keine

<strong>Befehlsoptionen</strong>:
   <dl>
   <dt>REPO_NAME (erforderlich)</dt>
   <dd>Der Name des Repositorys, das entfernt werden soll.</dd>
   </dl>

<strong>Beispiele</strong>:

Repository `IBM Cloud-repo` aus der Befehlszeilenschnittstelle von {{site.data.keyword.Bluemix_notm}} entfernen:

```
ibmcloud plugin repo-remove IBM Cloud-repo
```

## ibmcloud plugin repo-plugins
{: #ibmcloud_plugin_repo_plugins}

Alle verfügbaren Plug-ins in allen hinzufügten Repositorys oder einem bestimmten Repository auflisten.

```
ibmcloud plugin repo-plugins [-r REPO_NAME]
```

<strong>Voraussetzungen</strong>: Keine

<strong>Befehlsoptionen</strong>:

   <dl>
   <dt>-r <i>REPO_NAME</i> (optional)</dt>
   <dd>Nur die Plug-ins im angegebenen Repository auflisten.</dd>
   </dl>

<strong>Beispiele</strong>:

Alle Plug-ins in allen hinzugefügten Repositorys auflisten:

```
ibmcloud plugin repo-plugins
```

Alle Plug-ins im Repository `IBM Cloud-repo` auflisten:

```
ibmcloud plugin repo-plugins -r IBM Cloud-repo
```

## ibmcloud plugin repo-plugin
{: #ibmcloud_plugin_repo_plugin}

Details eines Plug-ins im Repository anzeigen.

```
ibmcloud plugin repo-plugin PLUGIN_NAME [-r REPO_NAME]
```

<strong>Voraussetzungen</strong>: Keine

<strong>Befehlsoptionen</strong>:

   <dl>
   <dt>-r <i>REPO_NAME</i> (optional)</dt>
   <dd>Der Name des Repositorys. Wird kein Repository angegeben, verwendet der Befehl das Standardrepository des Plug-ins.</dd>
   </dl>

<strong>Beispiele</strong>:

Details des Plug-ins "IBM-Containers" im Repository "sample-repo" auflisten:

```
ibmcloud plugin repo-plugin IBM-Containers -r sample-repo
```

Details des Plug-ins "IBM-Containers" im Standardrepository auflisten

```
ibmcloud plugin repo-plugin IBM-Containers -r sample-repo
```

## ibmcloud plugin list
{: #ibmcloud_plugin_list}

Alle installierten Plug-ins in der {{site.data.keyword.Bluemix_notm}}-CLI auflisten.

```
ibmcloud plugin list
```

<strong>Voraussetzungen</strong>: Keine

## ibmcloud plugin show
{: #ibmcloud_plugin_show}

Details eines installierten Plug-ins anzeigen.

```
ibmcloud plugin show PLUGIN-NAME
```

<strong>Voraussetzungen</strong>: Keine

## ibmcloud plugin install
{: #ibmcloud_plugin_install}

Angegebene Version des Plug-ins aus dem angegebenen Pfad oder Repository in der {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle installieren.

```
ibmcloud plugin install PLUGIN_PATH|PLUGIN_NAME [-r REPO_NAME] [-v VERSION]
```

```
ibmcloud plugin install LOCAL-PATH/TO/PLUGIN | URL [-f]
```

Wird kein Repository angegeben, verwendet der Befehl das Standardrepository 'IBM Cloud' des Plug-ins.
Wenn keine Version angegeben wird, wählt der Befehl die neueste verfügbare Version zur Installation aus.

<strong>Voraussetzungen</strong>: Keine

<strong>Befehlsoptionen</strong>:

   <dl>
   <dt>PLUGIN_PATH|PLUGIN_NAME (erforderlich)</dt>
   <dd>Wenn -r <i>REPO_NAME</i> nicht angegeben wird, wird das Plug-in vom angegebenen lokalen Pfad oder der Remote URL installiert.</dd>
   <dt>-r <i>REPO_NAME</i> (optional)</dt>
   <dd>Der Name des Repositorys, in dem sich die Plug-in-Binärdatei befindet. Wird kein Repository angegeben, verwendet der Befehl das Standardrepository 'IBM Cloud' des Plug-ins.</dd>
   <dt>-v <i>VERSION</i> (optional)</dt>
   <dd>Die Version des Plug-ins, die installiert werden soll. Wird keine Angabe gemacht, wird die neueste Version des Plug-ins installiert. Diese Option ist nur gültig, wenn Sie das Plug-in aus dem Repository installieren.</dd>
   <dt>-f </dt>
   <dd>Installieren des Plug-ins ohne Bestätigung erzwingen.</dd>
    </dl>


Die {{site.data.keyword.Bluemix_notm}}-CLI trägt den offiziellen Repository-Namen `IBM Cloud`.

<strong>Beispiele</strong>:

Plug-in von der lokalen Datei installieren:

```
ibmcloud plugin install /downloads/new_plugin
```

Plug-in von der Remote URL installieren:

```
ibmcloud plugin install http://plugins.ng.bluemix.net/downloads/new_plugin
```

Plug-in 'container-service' der neuesten Version aus dem Repository 'IBM Cloud' installieren:

```
ibmcloud plugin install container-service -r IBM Cloud
```

oder einfach:

```
ibmcloud plugin install container-service
```

Plug-in 'container-service' mit der Version '0.1.425' aus dem offiziellen Plug-in-Repository installieren:

```
ibmcloud plugin install container-service -v 0.1.425
```

## ibmcloud plugin update
{: #ibmcloud_plugin_update}

Upgrade des Plug-ins aus einem Repository durchführen.

```
ibmcloud plugin update [PLUGIN NAME] [-r REPO_NAME] [-v VERSION] [--all]
```

Wird kein Repository angegeben, verwendet der Befehl das Standardrepository 'IBM Cloud' des Plug-ins.
Wenn keine Version angegeben wird, wählt der Befehl die neueste verfügbare Version zur Installation aus.

<strong>Voraussetzungen</strong>: Keine

<strong>Befehlsoptionen</strong>:
<dl>
 <dt>PLUGIN NAME</dt>
 <dd>Name des zu aktualisierenden Plug-ins. Wenn keine Angabe erfolgt, prüft der Befehl Upgrades für alle installierten Befehle.</dd>
 <dt>-r REPO_NAME</dt>
 <dd>Der Name des Repositorys, in dem sich die Plug-in-Binärdatei befindet. Wenn keine Angabe gemacht wird, verwendet der Befehl das Standardrepository 'IBM Cloud' des Plug-ins.</dd>
 <dt>-v <i>VERSION</i> (optional)</dt>
 <dd>Die Version des Plug-ins, auf die aktualisiert werden soll. Wenn keine Version angegeben wird, wird das Plug-in auf die neueste verfügbare Version aktualisiert.</dd>
 <dt>--all</dt>
 <dd>Alle verfügbaren Plug-ins aktualisieren</dd>
</dl>

<strong>Beispiele</strong>:

Offizielles Plug-in-Repository 'IBM Cloud' auf alle verfügbaren Upgrades prüfen:

```
ibmcloud plugin update -r IBM Cloud
```

oder einfach:

```
ibmcloud plugin update
```

Upgrade des Plug-ins 'container-service' im offiziellen Plug-in-Repository auf die neueste Version durchführen:

```
ibmcloud plugin update container-service
```

Plug-in 'container-service' im offiziellen Plug-in-Repository auf Version '0.1.440' aktualisieren:

```
ibmcloud plugin update container-service -v 0.1.440
```

## ibmcloud plugin uninstall
{: #ibmcloud_plugin_uninstall}

Angegebenes Plug-in in der {{site.data.keyword.Bluemix_notm}}-CLI deinstallieren.

```
ibmcloud plugin uninstall PLUGIN_NAME
```

<strong>Voraussetzungen</strong>: Keine

<strong>Befehlsoptionen</strong>:

   <dl>
   <dt>PLUGIN_NAME (erforderlich)</dt>
   <dd>Der Name des Plug-ins, das deinstalliert werden soll.</dd>
    </dl>

<strong>Beispiele</strong>:

Plug-in 'container-service' deinstallieren, das zuvor installiert wurde:

```
ibmcloud plugin uninstall container-service
```
