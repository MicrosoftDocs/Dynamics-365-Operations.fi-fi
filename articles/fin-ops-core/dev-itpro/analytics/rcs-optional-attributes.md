---
title: Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä
description: Tässä artikkelissa on tietoja sellaisten ER-muotojen suunnittelemisesta, joissa määritetään XML-määritteet jäsentämään saapuvat sähköiset asiakirjat XML-muodossa.
author: kfend
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: bd4e2d75a598dd36de8b2ce89e83789d87b3a72e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276623"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä

[!include [banner](../includes/banner.md)]

Voit suunnitella sähköisen raportoinnin (ER) muodot jäsentämään saapuvat sähköiset asiakirjat XML-muodossa. Tietyt XML-elementtien määritteet voidaan määrittää suunnitellussa ER-muodossa valinnaisina. Sen avulla voit käsitellä saapuvia tiedostoja asianmukaisesti riippumatta siitä, onko siinä kyseiset määritteet vai ei. Sitten voit käyttää näiden tiedostojen sisältöä sovelluksen tietojen päivittämiseen.

Saat lisätietoja tästä ominaisuudesta suorittamalla artikkelin [(RCS) Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä](tasks/import-files-xml-format-optional-attributes.md) vaiheet. Se on osa 7.5.4.3 IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen (10677) -liiketoimintaprosessia. Voit ladata kyseisen tehtäväoppaan ja liitetyt mallitiedostot [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684).


| Sisällön kuvaus       | Tiedosto                                                         |
|---------------------------|--------------------------------------------------------------|
| XML-muotoinen mallitiedosto | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| Tehtävän ohjaus                | RCS Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä.axtr |


Seuraavissa vaiheissa käsitellään, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi suunnitella ER-muotomäärityksen tuomaan valinnaisia määritteitä sisältävän XML-muotoisia tiedostoja. Näitä vaiheita varten on ensin suoritettava menettelyssä [Konfiguraation lähteiden luominen ja merkitseminen aktiivisiksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet. Ennen kuin aloitat, lataa ja tallenna IncomingDocumentToLearnHowToHandleOptionalAttributes.xml-tiedosto paikallisesti Microsoft Download Centeristä (https://go.microsoft.com/fwlink/?linkid=874684 ).

1. Valitse **Organisaation hallinto** > **Työtilat** > **Sähköinen raportointi**.
2. Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**. Jos konfiguraation lähde ei ole näkyvissä, suorita artikkelin [Konfiguraation lähteiden luominen ja merkitseminen aktiivisiksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheet.
3. Valitse **Raportointikonfiguraatiot**.

## <a name="create-a-new-data-model-configuration"></a>Uuden tietomallin konfiguraation luominen
1. Avaa valintaikkuna valitsemalla **Luo konfigurointi**.
2. Kirjoita **Nimi**-kenttään Xml-tiedoston tuontimalli.
3. Valitse **Luo konfiguraatio**.
4. Valitse **Suunnittelutoiminto**.
5. Avaa valintaikkuna valitsemalla **Uusi**.
6. Kirjoita **Nimi**-kenttään Juuri.
7. Valitse **Lisää**.
8. Avaa valintaikkuna valitsemalla **Uusi**.
9. Kirjoita **Nimi**-kenttään Luettelo.
10.    Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.
11.    Valitse **Lisää**.
12.    Avaa valintaikkuna valitsemalla **Uusi**.
13.    Kirjoita **Nimi**-kenttään Koodi.
14.    Valitse **Nimiketyyppi**-kentässä **Merkkijono**.
15.    Valitse **Lisää**.
16.    Valitse **Tallenna**.
17.    Sulje sivu.
18.    Valitse **Muuta tila**.
19.    Valitse **Valmis**.
20.    Valitse **OK**.

## <a name="create-a-format-for-data-import"></a>Tietojen tuontimuodon luominen
1. Avaa valintaikkuna valitsemalla **Luo konfigurointi**.
2. Kirjoita **Uusi**-kenttään Muoto perustuu tietomalliin Xml-tiedoston tuontimalli.
3. Kirjoita **Nimi**-kenttään Xml-tiedoston tuontimuoto. 
4. Valitse **Tukee tietojen tuontia** -kentässä **Kyllä**.
5. Valitse **Luo konfiguraatio**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Muodon suunnitteleminen jäsentämään saapuvan tiedosto xml-muodossa
1. Valitse **Suunnittelutoiminto**.
2. Avaa valintaikkuna valitsemalla **Lisää juuri**.
3. Valitse puussa **XML\Elementti**.
4. Kirjoita **Nimi**-kenttään root.
5. Valitse **OK**.
6. Avaa valintaikkuna valitsemalla **Lisää**.
7. Valitse puussa **XML\Elementti**.
8. Kirjoita **Nimi**-kenttään document.
9. Valitse **Monimuotoisuus**-kentässä **Yksi tai useita**.
10.    Valitse **OK**.
11.    Valitse puussa **root\document**.
12.    Avaa valintaikkuna valitsemalla **Lisää**.
13.    Valitse puussa **XML\Määrite**.
14.    Kirjoita **Nimi**-kenttään id.
15.    Valitse **OK**.
16.    Valitse **Tallenna**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Muodon yhdistämisen suunnitteleminen tallentamaan jäsennetty tieto tietomalliin
1.    Valitse **Yhdistä muoto malliin**.
2.    Valitse **Uusi**.
3.    Anna tai valitse **Määritys**-kentän arvo.
4.    Kirjoita **Nimi**-kenttään Yhdistäminen.
5.    Valitse **Tallenna**.
6.    Valitse **Suunnittelutoiminto**.
7.    Laajenna puussa **format**.
8.    Laajenna puussa **format\root: XML Element(root)**.
9.    Valitse puussa **format\root: XML Element(root)\document: XML Element 1..* (tiedosto)**.
10.    Valitse **Sido**.
11.    Laajenna puussa **format\root: XML Element(root)\document: XML Element 1..* (tiedosto)**.
12.    Valitse puussa **format\root: XML Element(root)\document: XML Element 1..* (tiedosto)\id**.
13.    Laajenna puussa **List = format.root.document**.
14.    Valitse puussa **List = format.root.document\Code**.
15.    Valitse **Sido**.
16.    Valitse **Tallenna**.
17.    Sulje sivu.

## <a name="run-format-mapping"></a>Muodon yhdistämisen suorittaminen
1. Valitse **Suorita**.
2. Valitse ensin **Selaa** ja sitten tiedosto **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Valitse **OK**.

> [!NOTE]
> Valittua tiedostoa ei ole tuotu, sillä muodon rakenne olettaa, että document-elementissä on id-määrite mutta tuodussa tiedostossa tätä määritettä ei ole.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Muodon rakenteen muokkaaminen käsittelemään xml-määritettä valinnaisena
1. Sulje sivu.
2. Laajenna puussa **root\document**.
3. Valitse puussa **root\document\id**.
4. Valitse **Puuttuvan määritteen tyhjä merkkijono** -kentässä **Kyllä**.
5. Valitse **Tallenna**.

## <a name="run-format-mapping-to-test-changes"></a>Muutosten testaaminen suorittamalla muodon yhdistäminen
1. Valitse **Yhdistä muoto malliin**.
2. Valitse **Suorita**.
3. Valitse ensin **Selaa** ja sitten tiedosto **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Valitse **OK**.
5. Tarkista luotu tiedosto. Huomaa, että sama tiedosto on tuotu, sillä muodon rakenne käsittelee document-elementit id-määritettä nyt valinnaisena.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
