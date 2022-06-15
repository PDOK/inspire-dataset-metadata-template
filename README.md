# INSPIRE DATASET METADATA TEMPLATE

[![](https://img.shields.io/badge/author-@arbakker-blue.svg?style=flat)](https://github.com/arbakker)

[![](https://img.shields.io/badge/gh--pages-readme-green?style=flat)](https://arbakker.github.io/inspire-dataset-metadata-template/)

Dit repository bevat:

- een [template](https://raw.githubusercontent.com/arbakker/inspire-dataset-metadata-template/master/inspire-dataset-metadata-template.xml) voor het eenvoudig aanmaken van een geldig INSPIRE dataset metadata record in [nationaalgeoregister.nl](https://nationaalgeoregister.nl/geonetwork/srv/dut/catalog.search#/home) (NGR)
- een [handleiding](https://arbakker.github.io/inspire-dataset-metadata-template/#handleiding) voor het invullen van dit template in de metadata editor van het [NGR](https://nationaalgeoregister.nl/geonetwork/srv/dut/catalog.search#/home)

Dit template is aangemaakt aan de hand van het [Nederlands metadata profiel op ISO 19115 voor geografie versie 2.1.0](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/), verder in het document benoemd als _spec_. 

## Handleiding

Deze handleiding beschrijft hoe een valide INSPIRE dataset metadata record aan te maken op basis van het door PDOK aangemaakte [*Template Nederlands metadata profiel op ISO 19115 voor geografie 2.1.0 - INSPIRE*](https://ngr.acceptatie.nationaalgeoregister.nl/geonetwork/srv/dut/catalog.search#/metadata/C2DFBDBC-5092-11E0-BA8E-B62DE0D72085).

### 1. Aanmaken nieuw metadata record op basis van template

- Log in op het [nationaalgeoregister.nl](https://nationaalgeoregister.nl/geonetwork/srv/dut/catalog.search#/home) en kies via het menu _Metadata beheer > Record toevoegen_
- Kies dan voor _Dataset_ als type document
- En _Template Nederlands metadata profiel op ISO 19115 voor geografie 2.1.0 - INSPIRE_ als template
- Kies de juiste groep voor het nieuwe metadata record
- En klik op _Aanmaken_

Na het aanmaken van het nieuwe metadata record wordt het nieuwe record geopend in de metadata editor van het NGR.

> **N.B.** Met het aanmaken van een nieuw dataset metadata record op basis van het _Template Nederlands metadata profiel op ISO 19115 voor geografie 2.1.0 - INSPIRE_ wordt automatisch al de categorie `Inspire` aan het nieuwe metadata record toegekend, zie ![image](https://user-images.githubusercontent.com/3216462/174043886-e88efc26-6848-48a0-abdd-b23aec2c9261.png)


### 2. Invullen velden nieuw metadata record

Deze invulinstructie gaat er vanuit dat de _Nederlands profiel_ view geselecteerd is in de metadata editor:

![image](https://user-images.githubusercontent.com/3216462/173834968-cbe80302-cb7c-436f-b2f1-7a96158ca5d0.png)

En gaat van boven naar beneden door de metadata editor (in _Nederlands profiel_ view) heen. 

Alle velden die ingevuld dienen te worden of toelichting behoeven zijn opgenomen in de invulinstructie. 

Velden die niet genoemd worden in de invulinstructie maar wel in de metadata editor zitten kunnen ongewijzigd worden overgenomen, net als velden waar achter vermeld staat _"Vaste waarde `$X`"_.

Velden in de invulinstructie waarachter vermeld staat _"Voor ingevulde waarde `$X`"_, kunnen over het algemeen ongewijzigd worden overgenomen, maar zal in sommige gevallen toch gewijzigd moeten worden. Controleer hiervoor de documentatie waar naar gelinkt wordt. 

Opmaak conventie:

- [**_Veldnaam met documentatie_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/) -  Veldnaam uit de NGR metadata editor met documentatie lemma in [Nederlands metadata profiel op ISO 19115 voor geografie versie 2.1.0](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/) met eventuele extra invulinstructie/documentatie. 
- **_Veldnaam zonder documentatie_**  - Veldnaam uit de NGR metadata editor, waarvoor geen documentatie lemma beschikbaar is in [Nederlands metadata profiel op ISO 19115 voor geografie versie 2.1.0](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/).
- `waarde` - Invulwaarde
- Headers corresponderen met de secties in de metadata editor bijvoorbeeld:

<figure>
  <img
  src="https://user-images.githubusercontent.com/3216462/174039366-d98ebe84-4738-4253-ba46-aca232ac22f8.png"
  alt="Sectie in NGR metadata editor">
 <figcaption><em>Sectie in NGR metadata editor</em></figcaption>
</figure>
<br/>
<br/>
<figure>
  <img
  src="https://user-images.githubusercontent.com/3216462/174039556-c37cd9f4-550d-46b8-b0c0-98016c37c422.png"
  alt="Dezelfde sectie in deze invulinstructie">
 <figcaption><em>Dezelfde sectie in deze invulinstructie</em></figcaption>
</figure>


#### 2.1 Downloads, views en links

1. **_Afbeelding (niet als zodanig gelabeld in metadata editor)_** - Vervang de placeholder voorbeeld weergave afbeelding met een van de dataset die beschreven wordt in dit metadata record. Aangeraden wordt vanuit PDOK om een afbeelding te kiezen met afmetingen van `500x500` pixels. Voorbeeld afbeelding kan op verschillende manieren gemaakt worden:
    - Vanuit de NGR metadata editor is er de mogelijkheid om een thumbnail te genereren op basis van een view service (werkte niet op moment van schrijven van deze handleiding)
    - Gebruik de [PDOK Thumbnail Generator](https://pdok.github.io/thumbnail-generator/)
    - Genereer een thumbnail met een desktop GIS programma
2. **_Hyperlinks_** -  Vervang beide links naar de service accesspoints, dus voor zowel de download als de view service. In het template zijn een **WMS** en **INSPIRE ATOM** placeholder service URL voor ingevuld, maar hier kunnen ook andere service protocollen gebruikt worden. Vul de volgende velden voor de hyperlink als volgt in:
    - [**_URL_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-29-url) - Service URL dat linkt naar een capabilities document (of INSPIRE Atom service feed). Bijvoorbeeld [`https://geodata.nationaalgeoregister.nl/rdinfo/wms?service=WMS&request=GetCapabilities`](https://geodata.nationaalgeoregister.nl/rdinfo/wms?service=WMS&request=GetCapabilities).
    - [**_Protocol_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-30-protocol) - Kies juiste waarde uit de lijst
    - [**_Naam_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-31-naam), in het geval van INSPIRE ontsluit één service typisch één dataset; in dat geval dient hier de titel van de service ingevuld te worden.  
    - [**_Omschrijving_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-32-omschrijving) - Vaste waarde `accessPoint`
    - **_Functie_** - Vaste waarde `information`, zie ook [_Metadata IR_](https://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf) en zoek op `CI_OnLineFunctionCode`
    - **_Applicatie profiel_** - Afhankelijk van het type service, zie [SpatialDataServiceType codelijst](https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceType) en zie voor meer informatie de [spec](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-32-omschrijving)


#### 2.2 Identificatie

1. [**_Titel van de bron_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-1-titel-van-de-bron) - Titel van de dataset, indien het een INSPIRE geharmoniseerde dataset is het gebruikelijk het achtervoegsel `(INSPIRE geharmoniseerd)` te gebruiken. Klik ook op het link icoontje om een achor toe te voegen. Aangeraden wordt om naar het metadata record van de dataset te verwijzen (dit is dus het metadata record wat nu aangemaakt wordt!). Gebruik dan de volgende waarde: `https://nationaalgeoregister.nl/geonetwork/srv/dut/csw?SERVICE=CSW&version=2.0.2&REQUEST=GetRecordById&elementSetName=full&OutputSchema=http://www.isotc211.org/2005/gmd&ID=${METADATA_IDENTIFIER}` waar `${METADATA_IDENTIFIER}` de metadata identifier is van het huidige metadata record. Deze is te zien via de XML view: ![image](https://user-images.githubusercontent.com/3216462/174069318-1973c329-d5d2-4a15-b391-b1d0253924cc.png)

3. [**_Datum van de bron_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#datum-van-de-bron)

##### 2.2.1 Beheer van de bron

1. **_Herzieningsfrequentie_** - Frequentie waarmee de data herzien wordt

---

1. [**_Unieke Identifier van de bron_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-4-unieke-identifier-van-de-bron) - Vul hier een valide UUID in, zie bijvoorbeeld [www.uuidgenerator.net](https://www.uuidgenerator.net/version4) voor het generen van een UUID
2. [**_Samenvatting_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-5-samenvatting)
3. [**_Status_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-6-status)
4. [**_Taal van de bron_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-7-taal-van-de-bron) - Vaste waarde `dut`
5. [**_Karakterset van de bron_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-8-karakterset-van-de-bron) - Voor ingevulde waarde `utf8`
6. [**_Onderwerp_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-9-onderwerp)

##### 2.2.2 Contactgegevens voor de data

1. [**Organisatie**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#Verantwoordelijke-organisatie-bron) - Vul de juiste organisatienaam in en vul in het veld eronder een URI naar representatief is voor de organisatie
2. [**_Email_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-11-verantwoordelijke-organisatie-bron-e-mail)
3. [**_Rol_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-12-verantwoordelijke-organisatie-bron-rol) - Vaste waarde `contactpunt`

--- 

1. [**_GEMET - INSPIRE themes, version 1.0_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-13-trefwoord) - Keyword uit INSPIRE [theme register](https://inspire.ec.europa.eu/theme)
2. [**_Ruimtelijke dekking_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-13-trefwoord) - Keyword uit INSPIRE [SpatialScope codelist](https://inspire.ec.europa.eu/metadata-codelist/SpatialScope/)
3. [**_GEMET - Concepts, version 2.4_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-13-trefwoord) - Optionele additionele keywords (bij voorkeur komen deze dus uit de [Gemet Concepts thesaurus](https://www.eionet.europa.eu/gemet/en/themes/))

#### 2.3 Ruimtelijke informatie

1. [**_Ruimtelijk schema_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-20-ruimtelijk-schema-van-de-bron)
2. Een van:
    - [**_Schaal_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-21-toepassingsschaal)
    - [**_Resolutie_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-22-resolutie)

> **N.B.** In het geval dat het veld [**_Resolutie_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-22-resolutie) gebruikt wordt dient het veld [**_Schaal_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-21-toepassingsschaal) verwijderd te worden. Verwijder deze door op het kruisje klikken naast het element. 

##### 2.3.1 Omgrenzende rechthoek  

1. [**_Kies een regio_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-25-omgrenzende-rechthoek)

---

1. [**_Ruimtelijk referentiesysteem_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-23-ruimtelijk-referentiesysteem)



#### 2.4 Gebruiks beperkingen

#### 2.4.1 Beperkingen

1. [**_Gebruiksbeperkingen_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-19-gebruiksbeperkingen) - Indien geen gebruiksbeperkingen vul dan `Geen gebruiksbeperkingen` in.

#### 2.5 Juridische toegangs beperkingen

Zie [spec](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-17-juridische-toegangsrestricties) voor uitleg. Template is voor ingevuld op basis van [_Voorbeeld 5_](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#example-5-xml-notatie-open-data-licentie-met-inspire) uit de spec. 

##### 2.5.1 Juridische toegangs beperkingen

Vaste waarde, indien gebruik wordt gemaakt van <https://creativecommons.org/publicdomain/mark/1.0/deed.nl> licentie.

##### 2.5.2 Juridische toegangsbeperkingen

Vaste waarde, indien gebruik wordt gemaakt van <https://creativecommons.org/publicdomain/mark/1.0/deed.nl> licentie.

#### 2.6 Distributie

##### 2.6.1 Distributie formaat 

1. [**_Naam distributie formaat_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-26-naam-distributie-formaat)
    - **_Text veld_** - Format `$THEMA_NAAM GML Application Schema`, bijvoorbeeld: `Protected Sites - GML Application Schema` 
    - **_URL Verwijzing_** - URL naar XSD van INSPIRE thema bijvoorbeeld:  `https://inspire.ec.europa.eu/schemas/ps/4.0/ProtectedSites.xsd`
2. [**_Versie distributie formaat_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-27-versie-distributie-formaat) - Voor ingevulde waarde:  `versie 4.0; GML, versie 3.2.1` (afhankelijk van versie XSD thema en GML)
3. [**_Specificatie distributie formaat_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-28-specificatie-distributie-formaat)
    - **_Text veld_** - Format `Data specificatie $THEMA_NAAM_NL`, bijvoorbeeld: `Data specificatie Beschermde gebieden` 
    - **_URL Verwijzing_** - URL INSPIRE technical guidance van thema, bijvoorbeeld: `http://inspire.ec.europa.eu/id/document/tg/ps`

#### 2.7 Data kwaliteit

1. [**_Niveau kwaliteits beschrijving_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-33-niveau-kwaliteitsbeschrijving) - Vaste waarde `dataset`
2. [**_Algemene beschrijving herkomst_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-34-algemene-beschrijving-herkomst)

##### 2.7.1 Domein consistentie / Conformiteit indicatie met de specificatie 1

Vooringevuld, zie [spec](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-35-specificatie). Is indicatie dat de dataset en bijbehorende services voldoen aan de INSPIRE richtlijnen, indien de checkbox **_Conformiteit indicatie met de specificatie_** is aangevinkt. Indien niet volledige voldaan wordt aan de INSPIRE richtlijnen kan in het veld [_**Verklaring**_](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-38-verklaring) worden aangeven waarom niet wordt voldaan aan de richtlijnen. 

##### 2.7.2 Domein consistentie / Conformiteit indicatie met de specificatie 2

Tweede **_Conformiteit indicatie met de specificatie_** element is om aan te geven dat dataset voldoet aan de datamodel behorend bij het INSPIRE data thema.

1. [**_Titel_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-35-specificatie)
    - **_URL verwijzing_** - URL naar pagina waar technical guidance voor data thema te downloaden is, bijvoorbeeld: `https://inspire.ec.europa.eu/id/document/tg/au`
3. [**_Specificatie datum_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-35-specificatie) - Laat type datum op `publicatie` staan en vul de publicatie datum van de Technical Guidance van het betreffende INSPIRE data thema
4. [**_Verklaring_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-38-verklaring) - Vul waarde in `Dataset voldoet aan specificatie` indien deze voldoen aan de specificatie, indien deze niet voldoet kan hier een reden worden opgegeven waarom niet wordt voldaan aan de specificatie. 



#### 2.8 Over de metadata

1. [**_Taal van de metadata_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-44-taal-van-de-metadata) - Vaste waarde `dut`
2. **_Metadata karakterset_** -  Vaste waarde `utf8` 
3. [**_Hiërarchisch niveau_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-46-hierarchieniveau) - Vaste waarde `dataset`

##### 2.8.1 Contact gegevens voor de metadata

1. [**Organisatie**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-48-verantwoordelijke-organisatie-metadata) - Vul de juiste organisatienaam in en vul in het veld eronder een URI naar representatief is voor de organisatie
2. [**_Email_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#metadata-elementen-uitwerking)
3. [**_Rol_**](https://docs.geostandaarden.nl/md/mdprofiel-iso19115/#x5-2-49-verantwoordelijke-organisatie-metadata-rol) - Vaste waarde `contactpunt`

Nadat alle velden zijn ingevuld 


### 3. Valideren met INSPIRE ETF validator

1. Navigeer met de browser naar de [INSPIRE Reference Validator](https://inspire.ec.europa.eu/validator/home/index.html)
2. Klik op _Test your data, services or metadata_
3. Selecteer bij _Select the INSPIRE resource you would like to test_ de waarde `Metadata`
4. Selecteer bij _Select the Technical Guidelines version_ de waarde `Version 2.0`
5. Selecteerd bij _Select the type of metadata record(s) to be tested_ de waarde `Data sets and data set series`
6. Vul de antispam filter in
7. Geef een referentie naar het zojuist aangemaakt metadata record op:
  - een url naar het XML document van de metadata, dus bijvoorbeeld: `https://ngr.acceptatie.nationaalgeoregister.nl/geonetwork/srv/dut/csw?SERVICE=CSW&version=2.0.2&REQUEST=GetRecordById&elementSetName=full&OutputSchema=http://www.isotc211.org/2005/gmd&ID=60a2a7c2-d5b3-4ad5-b562-c448695357fb`
  - download het XML metadata document vanuit het NGR en upload het bestand in het formulier (bijvoorbeeld in het geval het metadata record nog niet gepubliceerd is)
8. Bij een geslaagde validatie wordt het volgende scherm getoond (`PASSED_MANUAL` geeft aan dat de validatie geslaagd is, maar dat een aantal zaken nog handmatig gecontroleerd moeten worden):

![image](https://user-images.githubusercontent.com/3216462/174074851-c700bfdf-72c4-406e-bca1-f4243a95cdbc.png)






---

> **N.B.** Onderstaande `CSS` is nodig voor styling van de gh-pages page.

<style>
a strong em{
    color: #0366d6
}
</style>

