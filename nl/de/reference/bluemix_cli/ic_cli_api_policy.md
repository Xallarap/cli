---

copyright:

  years: 2018


lastupdated: "2018-06-21"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:tip: .tip}

# CLI-Befehle zur Verwaltung von API-Schlüsseln und Richtlinien
{: #ibmcloud_commands_iam}

<table summary="ibmcloud-Befehle zur Verwaltung von API-Schlüsseln und Richtlinien.">
 <caption>Tabelle 1. Befehle zur Verwaltung von API-Schlüsseln und Richtlinienn</caption>
  <thead>
  <th colspan="5">Befehle zur Verwaltung von API-Schlüsseln und Richtlinien</th>
  </thead>
  <tbody>
  <tr>
   <td>[ibmcloud iam service-ids](ic_cli_api_policy.html#ibmcloud_iam_service_ids)</td>
   <td>[ibmcloud iam service-id](ic_cli_api_policy.html#ibmcloud_iam_service_id)</td>
   <td>[ibmcloud iam service-id-create](ic_cli_api_policy.html#ibmcloud_iam_service_id_create)</td>
   <td>[ibmcloud iam service-id-update](ic_cli_api_policy.html#ibmcloud_iam_service_id_update)</td>
   <td>[ibmcloud iam service-id-delete](ic_cli_api_policy.html#ibmcloud_iam_service_id_delete)</td>
  </tr>
  <tr>
   <td>[ibmcloud iam service-id-lock](ic_cli_api_policy.html#ibmcloud_iam_service_id_lock)</td>
   <td>[ibmcloud iam service-id-unlock](ic_cli_api_policy.html#ibmcloud_iam_service_id_unlock)</td>
   <td>[ibmcloud iam api-keys](ic_cli_api_policy.html#ibmcloud_iam_api_keys)</td>
   <td>[ibmcloud iam api-key-create](ic_cli_api_policy.html#ibmcloud_iam_api_key_create)</td>
   <td>[ibmcloud iam api-key-delete](ic_cli_api_policy.html#ibmcloud_iam_api_key_delete)</td>
  </tr>
  <tr>
   <td>[ibmcloud iam api-key-update](ic_cli_api_policy.html#ibmcloud_iam_api_key_update)</td>
   <td>[ibmcloud iam api-key-lock](ic_cli_api_policy.html#ibmcloud_iam_api_key_lock)</td>
   <td>[ibmcloud iam api-key-unlock](ic_cli_api_policy.html#ibmcloud_iam_api_key_unlock)</td>
   <td>[ibmcloud iam service-api-keys](ic_cli_api_policy.html#ibmcloud_iam_service_api_keys)</td>
   <td>[ibmcloud iam service-api-key](ic_cli_api_policy.html#ibmcloud_iam_service_api_key)</td>
  </tr>
  <tr>
   <td>[ibmcloud iam service-api-key-create](ic_cli_api_policy.html#ibmcloud_iam_service_api_key_create)</td>
   <td>[ibmcloud iam service-api-key-update](ic_cli_api_policy.html#ibmcloud_iam_service_api_key_update)</td>
   <td>[ibmcloud iam service-api-key-delete](ic_cli_api_policy.html#ibmcloud_iam_service_api_key_delete)</td>
   <td>[ibmcloud iam service-api-key-lock](ic_cli_api_policy.html#ibmcloud_iam_service_api_key_lock)</td>
   <td>[ibmcloud iam service-api-key-unlock](ic_cli_api_policy.html#ibmcloud_iam_service_api_key_unlock)</td>
  </tr>
  <tr>
    <td>[ibmcloud iam service-policies](ic_cli_api_policy.html#ibmcloud_iam_service_policies)</td>
    <td>[ibmcloud iam service-policy](ic_cli_api_policy.html#ibmcloud_iam_service_policy)</td>
    <td>[ibmcloud iam service-policy-create](ic_cli_api_policy.html#ibmcloud_iam_service_policy_create)</td>
    <td>[ibmcloud iam service-policy-update](ic_cli_api_policy.html#ibmcloud_iam_service_policy_update)</td>
    <td>[ibmcloud iam service-policy-delete](ic_cli_api_policy.html#ibmcloud_iam_service_policy_delete)</td>
  </tr>
  <tr>
   <td>[ibmcloud iam user-policies](ic_cli_api_policy.html#ibmcloud_iam_user_policies)</td>
   <td>[ibmcloud iam user-policy](ic_cli_api_policy.html#ibmcloud_iam_user_policy)</td>
   <td>[ibmcloud iam user-policy-create](ic_cli_api_policy.html#ibmcloud_iam_user_policy_create)</td>
   <td>[ibmcloud iam user-policy-update](ic_cli_api_policy.html#ibmcloud_iam_user_policy_update)</td>
   <td>[ibmcloud iam user-policy-delete](ic_cli_api_policy.html#ibmcloud_iam_user_policy_delete)</td>
  </tr>
  <tr>
     <td>[ibmcloud iam oauth-tokens](ic_cli_api_policy.html#ibmcloud_iam_oauth_tokens)</td>
     <td>[ibmcloud iam dedicated-id-disconnect](ic_cli_api_policy.html#ibmcloud_iam_dedicated_id_disconnect)</td>
     <td>[ibmcloud iam authorization-policy-create](ic_cli_api_policy.html#ibmcloud_iam_authorization_policy_create)</td>
     <td>[ibmcloud iam authorization-policy-delete](ic_cli_api_policy.html#ibmcloud_iam_authorization_policy_delete)</td>
     <td>[ibmcloud iam authorization-policy](ic_cli_api_policy.html#ibmcloud_iam_authorization_policy)</td>
  </tr>
  <tr>
     <td>[ibmcloud iam authorization-policies](ic_cli_api_policy.html#ibmcloud_iam_authorization_policies)</td>
  </tr>
  </tbody>
  </table>
  
  ### ibmcloud iam service-ids
{: #ibmcloud_iam_service_ids}

Alle Service-IDs auflisten

```
ibmcloud iam service-ids [--uuid]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>--uuid</dt>
  <dd>Nur UUID der Service-IDs anzeigen</dd>
</dl>

<strong>Beispiele</strong>:
UUID aller Service-IDs des aktuellen Kontos auflisten

```
ibmcloud iam service-ids --uuid
```

### ibmcloud iam service-id
{: #ibmcloud_iam_service_id}

Details einer Service-ID anzeigen

```
ibmcloud iam service-id (NAME|UUID) [--uuid]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>NAME (erforderlich)</dt>
  <dd>Der Name des Service, gegenseitig ausschließend mit UUID</dd>
  <dt>UUID (erforderlich)</dt>
  <dd>Die UUID des Service, gegenseitig ausschließend mit NAME</dd>
  <dt>--uuid</dt>
  <dd>Die UUID der Service-ID anzeigen</dd>
</dl>

<strong>Beispiele</strong>:

Details der Service-ID `sample-test` anzeigen

```
ibmcloud iam service-id sample-test
```
Details der Service-ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` anzeigen

```
ibmcloud iam service-id ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### ibmcloud iam service-id-create
{: #ibmcloud_iam_service_id_create}

Service-ID erstellen

```
ibmcloud iam service-id-create NAME [-d, --description DESCRIPTION] [--lock]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>NAME (erforderlich)</dt>
  <dd>Der Name des Service</dd>
  <dt>-d, --description</dt>
  <dd>Die Beschreibung der Service-ID</dd>
  <dt>--lock</dt>
  <dd>Die Service-ID bei der Erstellung sperren</dd>
</dl>

<strong>Beispiele</strong>:

Service-ID mit dem Servicenamen `sample-test` und der Beschreibung `hello, world!` erstellen

```
ibmcloud iam service-id-create sample-test -d 'hello, world!'
```

Gesperrte Service-ID mit dem Servicenamen `sample-test` und der Beschreibung `hello, world!` erstellen

```
ibmcloud iam service-id-create sample-test -d 'hello, world!' --lock
```

### ibmcloud iam service-id-update

{: #ibmcloud_iam_service_id_update}
Service-ID aktualisieren

```
ibmcloud iam service-id-update (NAME|UUID) [-n, --name NEW_NAME] [-d, --description DESCRIPTION] [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>NAME (erforderlich)</dt>
  <dd>Der Name des Service, gegenseitig ausschließend mit UUID</dd>
  <dt>UUID (erforderlich)</dt>
  <dd>Die UUID des Service, gegenseitig ausschließend mit NAME</dd>
  <dt>-n, --name</dt>
  <dd>Der neue Name des Service</dd>
  <dt>-d, --description</dt>
  <dd>Die neue Beschreibung des Service</dd>
  <dt>-f, --force</dt>
  <dd>Aktualisierung ohne Bestätigung</dd>
</dl>

<strong>Beispiele</strong>:

Service-ID `sample-test` ohne Bestätigung in `sample-test-2` umbenennen

```
ibmcloud iam service-id-update sample-test -n sample-test-2 -f
```

Beschreibung des Service `sample-test` aktualisieren

```
ibmcloud iam service-id-update sample-test -d 'hello, friend!'
```

Service-ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` mit neuer Beschreibung in `sample-test-3` umbenennen

```
ibmcloud iam service-id-update ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 -n sample-test-3 -d 'hello, my friends!'
```

### ibmcloud iam service-id-delete
{: #ibmcloud_iam_service_id_delete}

Service-ID löschen

```
ibmcloud iam service-id-delete (NAME|UUID) [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>NAME (erforderlich)</dt>
  <dd>Der Name des Service, gegenseitig ausschließend mit UUID</dd>
  <dt>UUID (erforderlich)</dt>
  <dd>Die UUID des Service, gegenseitig ausschließend mit NAME</dd>
  <dt>-f, --force</dt>
  <dd>Löschen ohne Bestätigung</dd>
</dl>

<strong>Beispiele</strong>:

Service-ID `sample-teset` ohne Bestätigung löschen

```
ibmcloud iam service-id-delete sample-teset -f
```

Service-ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` löschen

```
ibmcloud iam service-id-delete ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### ibmcloud iam service-id-lock
{: #ibmcloud_iam_service_id_lock}

Service-ID sperren

```
ibmcloud iam service-id-lock (NAME|UUID) [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>NAME (erforderlich)</dt>
  <dd>Der Name des Service, gegenseitig ausschließend mit UUID</dd>
  <dt>UUID (erforderlich)</dt>
  <dd>Die UUID des Service, gegenseitig ausschließend mit NAME</dd>
  <dt>-f, --force</dt>
  <dd>Sperren ohne Bestätigung</dd>
</dl>

<strong>Beispiele</strong>:

Service-ID `sample-teset` ohne Bestätigung sperren

```
ibmcloud iam service-id-lock sample-teset -f
```

Service-ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` sperren

```
ibmcloud iam service-id-lock ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### ibmcloud iam service-id-unlock
{: #ibmcloud_iam_service_id_unlock}

Service-ID entsperren

```
ibmcloud iam service-id-unlock (NAME|UUID) [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>NAME (erforderlich)</dt>
  <dd>Der Name des Service, gegenseitig ausschließend mit UUID</dd>
  <dt>UUID (erforderlich)</dt>
  <dd>Die UUID des Service, gegenseitig ausschließend mit NAME</dd>
  <dt>-f, --force</dt>
  <dd>Entsperren ohne Bestätigung</dd>
</dl>

<strong>Beispiele</strong>:

Service-ID `sample-teset` ohne Bestätigung entsperren

```
ibmcloud iam service-id-unlock sample-teset -f
```

Service-ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` entsperren

```
ibmcloud iam service-id-unlock ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### ibmcloud iam api-keys
{: #ibmcloud_iam_api_keys}

Alle API-Schlüssel der {{site.data.keyword.Bluemix_notm}}-Plattform auflisten

```
ibmcloud iam api-keys
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung

### ibmcloud iam api-key-create
{: #ibmcloud_iam_api_key_create}

Neuen API-Schlüssel für {{site.data.keyword.Bluemix_notm}}-Plattform erstellen

```
ibmcloud iam api-key-create NAME [-d DESCRIPTION] [--file FILE] [--lock]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung

<strong>Befehlsoptionen:</strong>
<dl>
<dt>NAME (erforderlich)</dt>
<dd>Der Name des zu erstellenden API-Schlüssels.</dd>
<dt>-d <i>DESCRIPTION</i> (optional)</dt>
<dd>Die Beschreibung des API-Schlüssels</dd>
<dt>--file <i>FILE</i></dt>
<dd>Informationen zu API-Schlüssel in angegebener Datei speichern. Wenn nicht festgelegt, wird der JSON-Inhalt angezeigt.</dd>
<dt>--lock</dt>
<dd>API-Schlüssel bei der Erstellung sperren</dd>
</dl>

<strong>Beispiele</strong>:

API-Schlüssel erstellen und in einer Datei speichern

```
ibmcloud iam api-key-create MyKey -d "this is my API key" --file key_file
```

Gesperrten API-Schlüssel mit dem Namen "test-key" erstellen

```
ibmcloud iam api-key-create test-key --lock
```

### ibmcloud iam api-key-update
{: #ibmcloud_iam_api_key_update}

API-Schlüssel der {{site.data.keyword.Bluemix_notm}}-Plattform aktualisieren

```
ibmcloud iam api-key-update (NAME|UUID) [-n name] [-d description]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung

<strong>Befehlsoptionen:</strong>
<dl>
<dt>NAME (erforderlich)</dt>
<dd>Der alte Name des zu aktualisierenden API-Schlüssels, gegenseitig ausschließend mit UUID</dd>
<dt>UUID (erforderlich)</dt>
<dd>Die UUID des zu aktualisierenden API-Schlüssels, gegenseitig ausschließend mit NAME</dd>
<dt>-n <i>NAME</i> (optional)</dt>
<dd>Der neue Name des API-Schlüssels</dd>
<dt>-d <i>DESCRIPTION</i> (optional)</dt>
<dd>Die neue Beschreibung des API-Schlüssels</dd>
</dl>

<strong>Beispiele</strong>:

Beschreibung eines API-Schlüssels aktualisieren:

```
ibmcloud iam api-key-update MyKey -d "the new description of my key"
```

### ibmcloud api-key-delete
{: #ibmcloud_iam_api_key_delete}

API-Schlüssel der {{site.data.keyword.Bluemix_notm}}-Plattform löschen

```
ibmcloud iam api-key-delete (NAME|UUID) [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung

<strong>Befehlsoptionen:</strong>
<dl>
<dt>NAME (erforderlich)</dt>
<dd>Der Name des zu löschenden API-Schlüssels, gegenseitig ausschließend mit UUID</dd>
<dt>UUID (erforderlich)</dt>
<dd>Die UUID des zu löschenden API-Schlüssels, gegenseitig ausschließend mit NAME</dd>
<dt>-f, --force</dt>
<dd>Löschung ohne Bestätigung erzwingen.</dd>
</dl>

### ibmcloud api-key-lock
{: #ibmcloud_iam_api_key_lock}

API-Schlüssel der Plattform sperren

```
ibmcloud iam api-key-lock (NAME|UUID) [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung

<strong>Befehlsoptionen:</strong>
<dl>
<dt>NAME (erforderlich)</dt>
<dd>Der Name des zu sperrenden API-Schlüssels, gegenseitig ausschließend mit UUID</dd>
<dt>UUID (erforderlich)</dt>
<dd>Die UUID des zu sperrenden API-Schlüssels, gegenseitig ausschließend mit NAME</dd>
<dt>-f, --force</dt>
<dd>Sperren ohne Bestätigung erzwingen.</dd>
</dl>

<strong>Beispiele</strong>:

API-Schlüssel "test-api-key" sperren

```
ibmcloud iam api-key-lock test-api-key
```

API-Schlüssel mit der angegebenen UUID ohne Bestätigung sperren

```
ibmcloud iam api-key-lock ApiKey-18f773b0-db53-43f1-ad68-92c667c218fe --force
```

### ibmcloud api-key-unlock
{: #ibmcloud_iam_api_key_unlock}

API-Schlüssel der Plattform entsperren

```
ibmcloud iam api-key-unlock (NAME|UUID) [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung

<strong>Befehlsoptionen:</strong>
<dl>
<dt>NAME (erforderlich)</dt>
<dd>Der Name des zu entsperrenden API-Schlüssels, gegenseitig ausschließend mit UUID</dd>
<dt>UUID (erforderlich)</dt>
<dd>Die UUID des zu entsperrenden API-Schlüssels, gegenseitig ausschließend mit NAME</dd>
<dt>-f, --force</dt>
<dd>Entsperren ohne Bestätigung erzwingen.</dd>
</dl>

<strong>Beispiele</strong>:

API-Schlüssel "test-api-key" entsperren

```
ibmcloud iam api-key-unlock test-api-key
```

API-Schlüssel mit der angegebenen UUID ohne Bestätigung entsperren

```
ibmcloud iam api-key-unlock ApiKey-18f773b0-db53-43f1-ad68-92c667c218fe --force
```

### ibmcloud iam service-api-keys
{: #ibmcloud_iam_service_api_keys}

Alle API-Schlüssel eines Service auflisten

```
ibmcloud iam service-api-keys (SERVICE_ID_NAME|SERVICE_ID_UUID) [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>SERVICE_ID_NAME (erforderlich)</dt>
  <dd>Der Name der Service-ID, gegenseitig ausschließend mit SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (erforderlich)</dt>
  <dd>Die UUID der Service-ID, gegenseitig ausschließend mit SERVICE_ID_NAME</dd>
  <dt>-f, --force</dt>
  <dd>Die Service-API-Schlüssel ohne Bestätigung anzeigen</dd>
</dl>

<strong>Beispiele</strong>:

Alle API-Schlüssel des Service `sample-service` auflisten

```
ibmcloud iam service-api-keys sample-service
```

### ibmcloud iam service-api-key
{: #ibmcloud_iam_service_api_key}

Details eines Service-API-Schlüssels auflisten

```
ibmcloud iam service-api-key (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID) [--uuid] [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>APIKEY_NAME (erforderlich)</dt>
  <dd>Der Name des API-Schlüssels, gegenseitig ausschließend mit APIKEY_UUID</dd>
  <dt>APIKEY_UUID (erforderlich)</dt>
  <dd>Die UUID des API-Schlüssels, gegenseitig ausschließend mit APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (erforderlich)</dt>
  <dd>Der Name der Service-ID, gegenseitig ausschließend mit SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (erforderlich)</dt>
  <dd>Die UUID der Service-ID, gegenseitig ausschließend mit SERVICE_ID_NAME</dd>
  <dt>--uuid</dt>
  <dd>Die UUID des Service-API-Schlüssels anzeigen</dd>
  <dt>-f, --force</dt>
  <dd>Den Service-API-Schlüssel ohne Bestätigung anzeigen</dd>
</dl>

<strong>Beispiele</strong>:

Details des Service-API-Schlüssels `sample-key` des Service `sample-service` anzeigen:

```
ibmcloud iam service-api-key sample-key sample-service
```

### ibmcloud iam service-api-key-create
{: #ibmcloud_iam_service_api_key_create}

Service-API-Schlüssel erstellen

```
ibmcloud iam service-api-key-create NAME (SERVICE_ID_NAME|SERVICE_ID_UUID) [-d, --description DESCRIPTION] [--file FILE] [-f, --force] [--lock]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>NAME (erforderlich)</dt>
  <dd>Der Name der Service-ID oder des neu erstellten Service-API-Schlüssels</dd>
  <dt>SERVICE_ID_NAME (erforderlich)</dt>
  <dd>Der Name der Service-ID, gegenseitig ausschließend mit SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (erforderlich)</dt>
  <dd>Die UUID der Service-ID, gegenseitig ausschließend mit SERVICE_ID_NAME</dd>
  <dt>-d, --description</dt>
  <dd>Die Beschreibung des API-Schlüssels</dd>
  <dt>--file</dt>
  <dd>Informationen zu API-Schlüssel in angegebener Datei speichern. Wenn nicht festgelegt, wird der JSON-Inhalt angezeigt.</dd>
  <dt>-f, --force</dt>
  <dd>Erstellung ohne Bestätigung erzwingen</dd>
</dl>

<strong>Beispiele</strong>:

Service-API-Schlüssel `sample-key` für Service `sample-service` ohne Bestätigung erstellen:

```
ibmcloud iam service-api-key-create sample-key sample-service -f
```

### ibmcloud iam service-api-key-update
{: #ibmcloud_iam_service_api_key_update}

Service-API-Schlüssel aktualisieren

```
ibmcloud iam service-api-key-update (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID)  [-n, --name NEW_NAME] [-d, --description DESCRIPTION] [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>APIKEY_NAME (erforderlich)</dt>
  <dd>Der Name des API-Schlüssels, gegenseitig ausschließend mit APIKEY_UUID</dd>
  <dt>APIKEY_UUID (erforderlich)</dt>
  <dd>Die UUID des API-Schlüssels, gegenseitig ausschließend mit APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (erforderlich)</dt>
  <dd>Der Name der Service-ID, gegenseitig ausschließend mit SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (erforderlich)</dt>
  <dd>Die UUID der Service-ID, gegenseitig ausschließend mit SERVICE_ID_NAME</dd>
  <dt>-n, --name</dt>
  <dd>Der neue Name des Service-API-Schlüssels</dd>
  <dt>-d, --description</dt>
  <dd>Die neue Beschreibung des Service-API-Schlüssels</dd>
  <dt>-f, --force</dt>
  <dd>Aktualisierung ohne Bestätigung</dd>
</dl>

<strong>Beispiele</strong>:

Service-API-Schlüssel `sample-key` in `new-sample-key` umbenennen:

```
ibmcloud iam service-api-key-update sample-key sample-service -n new-sample-key
```

### ibmcloud iam service-api-key-delete
{: #ibmcloud_iam_service_api_key_delete}

Service-API-Schlüssel löschen

```
ibmcloud iam service-api-key-delete (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID) [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>APIKEY_NAME (erforderlich)</dt>
  <dd>Der Name des API-Schlüssels, gegenseitig ausschließend mit APIKEY_UUID</dd>
  <dt>APIKEY_UUID (erforderlich)</dt>
  <dd>Die UUID des API-Schlüssels, gegenseitig ausschließend mit APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (erforderlich)</dt>
  <dd>Der Name der Service-ID, gegenseitig ausschließend mit SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (erforderlich)</dt>
  <dd>Die UUID der Service-ID, gegenseitig ausschließend mit SERVICE_ID_NAME</dd>
  <dt>-f, --force</dt>
  <dd>Löschen ohne Bestätigung</dd>
</dl>

<strong>Beispiele</strong>:

Service-API-Schlüssel `sample-key` der Service-ID `sample-service` löschen:

```
ibmcloud iam service-api-key-delete sample-key sample-service
```

### ibmcloud iam service-api-key-lock
{: #ibmcloud_iam_service_api_key_lock}

Service-API-Schlüssel sperren

```
ibmcloud iam service-api-key-lock (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID) [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>APIKEY_NAME (erforderlich)</dt>
  <dd>Der Name des API-Schlüssels, gegenseitig ausschließend mit APIKEY_UUID</dd>
  <dt>APIKEY_UUID (erforderlich)</dt>
  <dd>Die UUID des API-Schlüssels, gegenseitig ausschließend mit APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (erforderlich)</dt>
  <dd>Der Name der Service-ID, gegenseitig ausschließend mit SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (erforderlich)</dt>
  <dd>Die UUID der Service-ID, gegenseitig ausschließend mit SERVICE_ID_NAME</dd>
  <dt>-f, --force</dt>
  <dd>Sperren ohne Bestätigung</dd>
</dl>

<strong>Beispiele</strong>:

Service-API-Schlüssel `sample-key` der Service-ID `sample-service` sperren:

```
ibmcloud iam service-api-key-lock sample-key sample-service
```

### ibmcloud iam service-api-key-unlock
{: #ibmcloud_iam_service_api_key_unlock}

Service-API-Schlüssel entsperren

```
ibmcloud iam service-api-key-unlock (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID) [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>APIKEY_NAME (erforderlich)</dt>
  <dd>Der Name des API-Schlüssels, gegenseitig ausschließend mit APIKEY_UUID</dd>
  <dt>APIKEY_UUID (erforderlich)</dt>
  <dd>Die UUID des API-Schlüssels, gegenseitig ausschließend mit APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (erforderlich)</dt>
  <dd>Der Name der Service-ID, gegenseitig ausschließend mit SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (erforderlich)</dt>
  <dd>Die UUID der Service-ID, gegenseitig ausschließend mit SERVICE_ID_NAME</dd>
  <dt>-f, --force</dt>
  <dd>Entsperren ohne Bestätigung</dd>
</dl>

<strong>Beispiele</strong>:

Service-API-Schlüssel `sample-key` der Service-ID `sample-service` entsperren:

```
ibmcloud iam service-api-key-unlock sample-key sample-service
```

### ibmcloud iam user-policies
{: #ibmcloud_iam_user_policies}

Richtlinien von Benutzer `name@example.com` auflisten:

```
ibmcloud iam user-policies name@example.com
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Zielkonto

<strong>Befehlsoptionen:</strong>
<dl>
<dt>USER_NAME (erforderlich)</dt>
<dd>Benutzername, zu dem die Richtlinien gehören</dd>
</dl>

<strong>Beispiele</strong>:

Richtlinien von Benutzer `name@example.com` auflisten:

```
ibmcloud iam user-policies name@example.com
```

### ibmcloud iam user-policy
{: #ibmcloud_iam_user_policy}

Details zu einer Benutzerrichtlinie anzeigen

```
ibmcloud iam user-policy USER_NAME POLICY_ID
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Zielkonto

<strong>Befehlsoptionen:</strong>
<dl>
<dt>USER_NAME (erforderlich)</dt>
<dd>Benutzername, zu dem die Richtlinie gehört</dd>
<dt>POLICY_ID (erforderlich)</dt>
<dd>Die ID der Richtlinie</dd>
</dl>

<strong>Beispiele</strong>:

Richtlinie `0bb730daa` des Benutzers `name@example.com` auflisten:

```
ibmcloud iam user-policy name@example.com 0bb730daa
```

### ibmcloud iam user-policy-create
{: #ibmcloud_iam_user_policy_create}

Benutzerrichtlinie erstellen

```
ibmcloud iam user-policy-create USER_NAME {--file JSON_FILE | --roles ROLE_NAME1,ROLE_NAME2... [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE_GUID] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]}
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Zielkonto

<strong>Befehlsoptionen:</strong>
<dl>
<dt>USER_NAME (erforderlich)</dt>
<dd>Der Benutzername, zu dem die Richtlinie gehört</dd>
<dt>--file <i>FILE</i> (optional)</dt>
<dd>Die JSON-Datei der Richtliniendefinition</dd>
<dt>--roles <i>ROLE_NAME1,ROLE_NAME2...</i> (optional)</dt>
<dd>Die Rollennamen der Richtliniendefinition. Führen Sie für unterstützte Rollen eines bestimmten Service 'ibmcloud iam roles --service SERVICE_NAME' aus. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
<dt>--service-name <i>SERVICE_NAME</i> (optional)</dt>
<dd>Der Servicename der Richtliniendefinition. Dieser kann nur mit dem Flag '--file' verwendet werden.</dd>
<dt>--serivce-instance <i>SERVICE_INSTANCE_GUID</i> (optional)</dt>
<dd>Die GUID der Serviceinstanz der Richtliniendefinition. Diese kann nur mit dem Flag '--file' verwendet werden.</dd>
<dt>--region <i>REGION</i> (optional)</dt>
<dd>Die Region der Richtliniendefinition. Diese kann nur mit dem Flag '--file' verwendet werden.</dd>
<dt>--resource-type <i>RESOURCE_TYPE</i> (optional)</dt>
<dd>Der Ressourcentyp der Richtliniendefinition. Dieser kann nur mit dem Flag '--file' verwendet werden.</dd>
<dt>--resource <i>RESOURCE</i> (optional)</dt>
<dd>Die Ressource der Richtliniendefinition. Diese kann nur mit dem Flag '--file' verwendet werden.</dd>
<dt>--resource-group-name <i>RESOURCE_GROUP_NAME</i> (optional)</dt>
<dd>Der Name der Ressourcengruppe. Dieser kann nur mit den Flags '--file', '--resource' und '--resource-group-id' verwendet werden.</dd>
<dt>--resource-group-id <i>RESOURCE_GROUP_ID</i> (optional)</dt>
<dd>Die ID der Ressourcengruppe. Diese kann nur mit den Flags '--file', '--resource' und '--resource-group-name' verwendet werden.</dd>
</dl>

<strong>Beispiele</strong>:

Benutzerrichtlinie für Benutzer `name@example.com` aus Richtlinien-JSON-Datei `policy.json` erstellen:

```
ibmcloud iam user-policy-create name@example.com --file @policy.json
```

`name@example.com` die Rolle `Administrator` für alle Ressourcen von `sample-service` zuweisen:

```
ibmcloud iam user-policy-create name@example.com --roles Administrator --service-name sample-service
```

`name@example.com` die Rolle `Editor` für die Ressource `key123` der Beispielserviceinstanz mit der GUID `d161aeea-fd02-40f8-a487-df1998bd69a9` in der Region `us-south` zuweisen:

```
ibmcloud iam user-policy-create name@example.com --roles Editor --service-name sample-service --service-instance d161aeea-fd02-40f8-a487-df1998bd69a9 --region us-south --resource-type key --resource key123
```

`name@example.com` die Rolle `Operator` für die Ressourcengruppe mit der ID `dda27e49d2a1efca58083a01dfde18f6` zuweisen:

```
ibmcloud iam user-policy-create name@example.com --roles Operator --resource-type resource-group --resource dda27e49d2a1efca58083a01dfde18f6
```

`name@example.com` die Rolle `Anzeigeberechtigter` für die Mitglieder der Ressourcengruppe `sample-resource-group` zuweisen:

```
ibmcloud iam user-policy-create name@example.com --roles Viewer --resource-group-name sample-resource-group
```

`name@example.com` die Rolle `Anzeigeberechtigter` für die Mitglieder der Ressourcengruppe mit der ID `dda27e49d2a1efca58083a01dfde18f6` zuweisen:

```
ibmcloud iam user-policy-create name@example.com --roles Viewer --resource-group-id dda27e49d2a1efca58083a01dfde18f6
```

### ibmcloud iam user-policy-update
{: #ibmcloud_iam_user_policy_update}

Benutzerrichtlinie aktualisieren

```
ibmcloud iam user-policy-update USER_NAME POLICY_ID {--file JSON_FILE | [--roles ROLE_NAME1,ROLE_NAME2...] [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE_GUID] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]}
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Zielkonto

<strong>Befehlsoptionen:</strong>
<dt>USER_NAME (erforderlich)</dt>
<dd>Der Benutzername, zu dem die Richtlinie gehört</dd>
<dt>POLICY_ID (erforderlich)</dt>
<dd>Die ID der zu aktualisierenden Richtlinie</dd>
<dt>--file <i>FILE</i> (optional)</dt>
<dd>Die JSON-Datei der Richtliniendefinition</dd>
<dt>--roles <i>ROLE_NAME1,ROLE_NAME2...</i> (optional)</dt>
<dd>Die Rollennamen der Richtliniendefinition. Führen Sie für unterstützte Rollen eines bestimmten Service 'ibmcloud iam roles --service SERVICE_NAME' aus. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
<dt>--service-name <i>SERVICE_NAME</i> (optional)</dt>
<dd>Der Servicename der Richtliniendefinition. Dieser kann nur mit dem Flag '--file' verwendet werden.</dd>
<dt>--serivce-instance <i>SERVICE_INSTANCE_GUID</i> (optional)</dt>
<dd>Die GUID der Serviceinstanz der Richtliniendefinition. Diese kann nur mit dem Flag '--file' verwendet werden.</dd>
<dt>--region <i>REGION</i> (optional)</dt>
<dd>Die Region der Richtliniendefinition. Diese kann nur mit dem Flag '--file' verwendet werden.</dd>
<dt>--resource-type <i>RESOURCE_TYPE</i> (optional)</dt>
<dd>Der Ressourcentyp der Richtliniendefinition. Dieser kann nur mit dem Flag '--file' verwendet werden.</dd>
<dt>--resource <i>RESOURCE</i> (optional)</dt>
<dd>Die Ressource der Richtliniendefinition. Diese kann nur mit dem Flag '--file' verwendet werden.</dd>
<dt>--resource-group-name <i>RESOURCE_GROUP_NAME</i> (optional)</dt>
<dd>Der Name der Ressourcengruppe. Dieser kann nur mit den Flags '--file', '--resource' und '--resource-group-id' verwendet werden.</dd>
<dt>--resource-group-id <i>RESOURCE_GROUP_ID</i> (optional)</dt>
<dd>Die ID der Ressourcengruppe. Diese kann nur mit den Flags '--file', '--resource' und '--resource-group-name' verwendet werden.</dd>
</dl>

<strong>Beispiele</strong>:

Benutzerrichtlinie mit der Benutzerrichtlinie in der JSON-Datei aktualisieren

```
ibmcloud iam user-policy-update name@example.com 0bb730daa --file @policy.json
```

Benutzerrichtlinie aktualisieren, um `name@example.com` die Rolle `Administrator` für alle Ressourcen von `sample-service` zu erteilen

```
ibmcloud iam user-policy-update name@example.com user-policy-id --roles Administrator --service-name sample-service
```

 Benutzerrichtlinie aktualisieren, um `name@example.com` die Rolle `Editor` für die Ressource `key123` der Beispielserviceinstanz mit der GUID `d161aeea-fd02-40f8-a487-df1998bd69a9` in der Region `us-south` zuzuweisen:

```
ibmcloud iam user-policy-update name@example.com --roles Editor --service-name sample-service --service-instance d161aeea-fd02-40f8-a487-df1998bd69a9 --region us-south --resource-type key --resource key123
```

Benutzerrichtlinie aktualisieren, um `name@example.com` die Rolle `Operator` für die Ressourcengruppe mit der ID `dda27e49d2a1efca58083a01dfde18f6` zuzuweisen:

```
ibmcloud iam user-policy-update name@example.com user-policy-id --roles Operator --resource-type resource-group --resource dda27e49d2a1efca58083a01dfde18f6
```

Benutzerrichtlinie aktualisieren, um `name@example.com` die Rolle `Anzeigeberechtigter` für die Mitglieder der Ressourcengruppe `sample-resource-group` zuzuweisen:

```
ibmcloud iam user-policy-update name@example.com user-policy-id --roles Viewer --resource-group-name sample-resource-group
```

Benutzerrichtlinie aktualisieren, um `name@example.com` die Rolle `Anzeigeberechtigter` für die Mitglieder der Ressourcengruppe mit der ID `dda27e49d2a1efca58083a01dfde18f6` zuzuweisen:

```
ibmcloud iam user-policy-update name@example.com user-policy-id --roles Viewer --resource-group-id dda27e49d2a1efca58083a01dfde18f6
```

### ibmcloud iam user-policy-delete
{: #ibmcloud_iam_user_policy_delete}

Benutzerrichtlinie löschen

```
ibmcloud iam user-policy-delete USER_ID POLICY_ID [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Zielkonto

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>-f, --force</dt>
  <dd>Benutzerrichtlinie ohne Bestätigung löschen</dd>
</dl>

<strong>Beispiele</strong>:
Richtlinie `user-policy-id` des Benutzers `name@example.com` löschen:

```
ibmcloud iam user-policy-delete name@example.com user-policy-id
```

Richtlinie `user-policy-id` des Benutzers `name@example.com` ohne Bestätigung löschen:

```
ibmcloud iam user-policy-delete name@example.com user-policy-id -f
```

### ibmcloud iam service-policies
{: #ibmcloud_iam_service_policies}

Alle Servicerichtlinien des angegebenen Service auflisten

```
ibmcloud iam service-policies SERVICE_ID [--json] [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>SERVICE_ID (erforderlich)</dt>
  <dd>Der Name oder die UUID der Service-ID</dd>
  <dt>-json</dt>
  <dd>Die Richtlinie im JSON-Format anzeigen</dd>
  <dt>-f, --force</dt>
  <dd>Die Servicerichtlinien ohne Bestätigung anzeigen</dd>
</dl>

<strong>Beispiele</strong>:

Richtlinien des Service `test` auflisten:

```
ibmcloud iam service-policies test
```
Richtlinien des Service `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` auflisten:

```
ibmcloud iam service-policies ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### ibmcloud iam service-policy
{: #ibmcloud_iam_service_policy}

Details zu einer Servicerichtlinie anzeigen

```
ibmcloud iam service-policy SERVICE_ID POLICY_ID [--json] [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>SERVICE_ID (erforderlich)</dt>
  <dd>Der Name oder die UUID der Service-ID</dd>
  <dt>POLICY_ID (erforderlich)</dt>
  <dd>Die ID der Servicerichtlinie<dd>
  <dt>-json</dt>
  <dd>Die Richtlinie im JSON-Format anzeigen</dd>
  <dt>-f, --force</dt>
  <dd>Die Servicerichtlinie ohne Bestätigung anzeigen</dd>
</dl>

<strong>Beispiele</strong>:

Richtlinie `140798e2-8ea7db3` des Service `test` anzeigen:

```
ibmcloud iam service-policies test 140798e2-8ea7db3
```
Richtlinie `140798e2-8ea7db3` des Service `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` anzeigen:

```
ibmcloud iam service-policies ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 140798e2-8ea7db3
```

### ibmcloud iam service-policy-create
{: #ibmcloud_iam_service_policy_create}

Servicerichtlinie erstellen

```
ibmcloud iam service-policy-create SERVICE_ID {--file JSON_FILE | -r, --roles ROLE_NAME1,ROLE_NAME2... [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE_GUID] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]} [-f, --force]",
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>SERVICE_ID (erforderlich)</dt>
  <dd>Der Name oder die UUID der Service-ID</dd>
  <dt>--file</dt>
  <dd>Die JSON-Datei der Richtliniendefinition. Dies kann nur mit den Flags '-r, --roles', '--service-name', '--service-instance', '--region', '--resource-type', '--resource', '--resource-group-name' und '--resource-group-id' verwendet werden.</dd>
  <dt>-r, --roles</dt>
  <dd>Die Rollennamen der Richtliniendefinition. Führen Sie für unterstützte Rollen eines bestimmten Service 'ibmcloud iam roles --service SERVICE_NAME' aus. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>--service-name</dt>
  <dd>Der Servicename der Richtliniendefinition. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>--service-instance <i>SERVICE_INSTANCE_GUID</i></dt>
  <dd>Die GUID der Serviceinstanz der Richtliniendefinition. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>-region</dt>
  <dd>Die Region der Richtliniendefinition. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>--resource-type</dt>
  <dd>Der Ressourcentyp der Richtliniendefinition. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>--resource</dt>
  <dd>Die Ressource der Richtliniendefinition. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>--resource-group-name</dt>
  <dd>Der Name der Ressourcengruppe. Diese Option ist gegenseitig ausschließend mit '--file' und '--resource-group-id'.</dd>
  <dt>--resource-group-id </dt>
  <dd>Die ID der Ressourcengruppe. Diese Option ist gegenseitig ausschließend mit '--file' und '--resource-group-name'.</dd>
  <dt>-f, --force</dt>
  <dd>Die Servicerichtlinie ohne Bestätigung erstellen</dd>
</dl>

<strong>Beispiele</strong>:

Servicerichtlinie aus JSON-Datei für Service `test` erstellen:

```
ibmcloud iam service-policy-create test --file @policy.json
```
Servicerichtlinie aus JSON-Datei für Service `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` erstellen:

```
ibmcloud iam service-policy-create ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 --file @policy.json
```

### ibmcloud iam service-policy-update
{: #ibmcloud_iam_service_policy_update}

Servicerichtlinie aktualisieren

```
ibmcloud iam service-policy-update SERVICE_ID POLICY_ID {--file JSON_FILE | [-r, --roles ROLE_NAME1,ROLE_NAME2...] [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE_GUID] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]} [-f, --force]",
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>SERVICE_ID (erforderlich)</dt>
  <dd>Der Name oder die UUID der Service-ID</dd>
  <dt>POLICY_ID (erforderlich)</dt>
  <dd>Die ID der Servicerichtlinie<dd>
  <dt>--file</dt>
  <dd>Die JSON-Datei der Richtliniendefinition. Diese kann nur mit den Flags '-r, --roles', '--service-name', '--service-instance', '--region', '--resource-type', '--resource', 'resource-group-name' und 'resource-group-id' verwendet werden.</dd>
  <dt>-r, --roles</dt>
  <dd>Die Rollennamen der Richtliniendefinition. Führen Sie für unterstützte Rollen eines bestimmten Service 'ibmcloud iam roles --service SERVICE_NAME' aus. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>-service-name</dt>
  <dd>Der Servicename der Richtliniendefinition. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>-service-instance <i>SERVICE_INSTANCE_GUID</i></dt>
  <dd>Die GUID der Serviceinstanz der Richtliniendefinition. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>-region</dt>
  <dd>Die Region der Richtliniendefinition. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>-resource-type</dt>
  <dd>Der Ressourcentyp der Richtliniendefinition. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>-resource</dt>
  <dd>Die Ressource der Richtliniendefinition. Diese Option ist gegenseitig ausschließend mit dem Flag '--file'.</dd>
  <dt>--resource-group-name</dt>
  <dd>Der Name der Ressourcengruppe. Diese Option ist gegenseitig ausschließend mit '--file' und '--resource-group-id'.</dd>
  <dt>--resource-group-id </dt>
  <dd>Die ID der Ressourcengruppe. Diese Option ist gegenseitig ausschließend mit '--file' und '--resource-group-name'.</dd>
  <dt>-f, --force</dt>
  <dd>Die Servicerichtlinie ohne Bestätigung aktualisieren</dd>
</dl>

<strong>Beispiele</strong>:

Servicerichtlinie `140798e2-8ea7db3` aus JSON-Datei für Service `test` aktualisieren:

```
ibmcloud iam service-policy-update test 140798e2-8ea7db3 --file @policy.json
```
Servicerichtlinie `140798e2-8ea7db3` aus JSON-Datei für Service `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` aktualisieren:

```
ibmcloud iam service-policy-update ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 140798e2-8ea7db3 --file @policy.json
```

### ibmcloud iam service-policy-delete
{: #ibmcloud_iam_service_policy_delete}

Servicerichtlinie löschen

```
ibmcloud iam service-policy-delete SERVICE_ID POLICY_ID [-f, --force]
```

<strong>Voraussetzungen</strong>: Endpunkt, Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>SERVICE_ID (erforderlich)</dt>
  <dd>Der Name oder die UUID der Service-ID</dd>
  <dt>POLICY_ID (erforderlich)</dt>
  <dd>Die ID der Servicerichtlinie<dd>
  <dt>-f, --force</dt>
  <dd>Löschen ohne Bestätigung</dd>
</dl>

<strong>Beispiele</strong>:

Richtlinie `140798e2-8ea7db3` des Service `test` löschen

```
ibmcloud iam service-policy-delete test 140798e2-8ea7db3
```
Richtlinie `140798e2-8ea7db3` des Service `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` löschen

```
ibmcloud iam service-policy-delete ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 140798e2-8ea7db3
```

### ibmcloud iam oauth-tokens
{: #ibmcloud_iam_oauth_tokens}

OAuth-Tokens für die aktuelle Sitzung abrufen und anzeigen

```
ibmcloud iam oauth-tokens
```

<strong>Voraussetzungen</strong>: Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
</dl>

<strong>Beispiele</strong>:

OAuth-Tokens aktualisieren und anzeigen

```
ibmcloud iam oauth-tokens
```

### ibmcloud iam dedicated-id-disconnect
{: #ibmcloud_iam_dedicated_id_disconnect}

Verbindung zwischen öffentlicher IBMid und dedizierter, von IBM unabhängiger ID trennen

```
ibmcloud iam dedicated-id-disconnect [-f, --force]
```

<strong>Voraussetzungen</strong>: Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>-f, --force</dt>
  <dd>Trennen ohne Bestätigung erzwingen</dd>
</dl>

### ibmcloud iam authorization-policy-create
{: #ibmcloud_iam_authorization_policy_create}

Berechtigungsrichtlinie erstellen, um den Zugriff einer Serviceinstanz auf eine andere Serviceinstanz zu ermöglichen.

```
ibmcloud iam authorization-policy-create SOURCE_SERVICE_NAME TARGET_SERVICE_NAME ROLE_NAME1,ROLE_NAME2... [—-source-service-instance SOURCE_SERVICE_INSTANCE_NAME] [—-target-service-instance TARGET_SERVICE_INSTANCE_NAME]
```

<strong>Voraussetzungen</strong>: Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>SOURCE_SERVICE_NAME</dt>
  <dd>Quellenservice, der für den Zugriff autorisiert werden kann.</dd>
  <dt>TARGET_SERVICE_NAME</dt>
  <dd>Zielservice, für dessen Zugriff der Quellenservice autorisiert werden kann.</dd>
  <dt>ROLE_NAME1,ROLE_NAME2...</dt>
  <dd>Die Rollen, die Zugriff für den Quellenservice bereitstellen.</dd>  
  <dt>—-source-service-instance SOURCE_SERVICE_INSTANCE_NAME</dt>
  <dd>Instanzname des Quellenservice. Wenn keine Angabe gemacht wird, erhalten alle Instanzen des Quellenservice Zugriffsberechtigung.</dd>
  <dt>—-target-service-instance TARGET_SERVICE_INSTANCE_NAME</dt>
  <dd>Instanzname des Zielservice. Wenn keine Angabe gemacht wird, erhalten alle Instanzen des Zielservice Zugriffsberechtigung.</dd>
</dl>

### ibmcloud iam authorization-policy-delete
{: #ibmcloud_iam_authorization_policy_delete}

Berechtigungsrichtlinie löschen.

```
ibmcloud iam authorization-policy-delete AUTHORIZATION_POLICY_ID [-f, --force]
```

<strong>Voraussetzungen</strong>: Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>AUTHORIZATION_POLICY_ID</dt>
  <dd>Die ID der zu löschenden Berechtigungsrichtlinie.</dd>
  <dt>-f, --force</dt>
  <dd>Löschen ohne Bestätigung erzwingen.</dd>
</dl>

### ibmcloud iam authorization-policy
{: #ibmcloud_iam_authorization_policy}

Details zu einer Berechtigungsrichtlinie anzeigen.

```
ibmcloud iam authorization-policy AUTHORIZATION_POLICY_ID
```

<strong>Voraussetzungen</strong>: Anmeldung, Ziel

<strong>Befehlsoptionen</strong>:
<dl>
  <dt>AUTHORIZATION_POLICY_ID</dt>
  <dd>Die ID der anzuzeigenden Berechtigungsrichtlinie.</dd>
</dl>

### ibmcloud iam authorization-policies
{: #ibmcloud_iam_authorization_policies}

Berechtigungsrichtlinien unter dem aktuellen Konto auflisten.

```
ibmcloud iam authorization-policies
```

<strong>Voraussetzungen</strong>: Anmeldung, Ziel
