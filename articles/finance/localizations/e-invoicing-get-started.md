---
title: Sähköisen laskutuksen käytön aloittaminen
description: Tässä aiheessa on tietoja, joiden avulla voit aloittaa sähköisen laskutuksen käytön Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
ms.date: 11/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ebef9cf97f7a91e0a2fd45f5e0e0fc620070b42a
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779691"
---
# <a name="get-started-with-electronic-invoicing"></a>Sähköisen laskutuksen käytön aloittaminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja, joiden avulla voit aloittaa sähköisen laskutuksen käytön. Tämä ohjeaihe opastaa sinut läpi yleiset RCS (Regulatory Configuration Services) -palvelun ja Dynamics 365 Financen konfiguraatiovaiheet ja antaa ohjeita, jotka on tehtävä, jotta liiketoimintaasiakirjat voidaan lähettää ja käsittelytulokset tarkistaa.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:

- Määritä Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS) ja Microsoft Dynamics 365 Finance- tai Dynamics 365 Supply Chain Management -ympäristö. Lisätietoja on ohjeaiheessa [Sähköisen laskutuksen hallinnan käytön aloittaminen](e-invoicing-get-started-service-administration.md).
- Luo organisaatiollesi konfiguraatiopalvelu. Lisätietoja on kohdassa [Määrityspalvelun luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Tuo sähköisen laskutuksen ominaisuus Microsoftin konfiguraatiopalvelusta. 

1. Kirjaudu sisään Regulatory Configuration Service (RCS) -tilillesi.
2. Valitse **Globalisaatio-ominaisuukset**-työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Tuo** ja valitse sitten **Synkronoi**.
4. Suodata **Konfigurointipalvelu**-sarake hakusanan **Microsoft** avulla.
5. Valitse sähköisen laskutusominaisuuden nimi taulukosta ja valitse sitten **Tuo**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Luo organisaation palveluntarjoajassa sähköisen laskutuksen ominaisuus

1. Valitse RCS:ssä **Globalisaatio-ominaisuudet** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
2. Valitse **Lisää** > **Perustuu aiempaan ominaisuuteen** ja anna **Nimi**-kentässä sähköisen lasktuksen ominaisuuden nimi.
3. Anna ominaisuuden kuvaus **Kuvaus**-kentässä.
4. Valitse **Perustoiminto**-kentästä tuotu sähköinen laskutusominaisuus Microsoftin konfiguraatiopalvelusta.
5. Valitse **Luo ominaisuus**.

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>Sähköisen laskutuksen maa-/aluekohtainen konfigurointi sähköisen laskutuksen ominaisuudelle

Maan tai alueen mukaan sähköinen laskutustoiminto saattaa edellyttää tiettyjä konfiguraatiota. 

> [!NOTE]
> Kun Suomen sähköinen laskutustoiminto otetaan käyttöön, hakujen sovelluskohtaisia parametreja ei tueta. Tämän ongelman voi ratkaista tarkastelemalla myynti- ja projektilaskumuotojen määrityksiä **Sähköinen raportointi** -moduulissa. Määritä **$PaymentMethodSubstitution**-yhdistämismäärityksen laskennallinen kenttä manuaalisesti ja sido kyseinen kenttä sitten myynti- ja projektilaskumuotojen **EpiPaymentMeansCode**-kenttään.
>
> Kun Italian sähköinen laskutustoiminto otetaan käyttöön, hakujen sovelluskohtaisia parametreja ei tueta. Ongelman voi ratkaista määrittämällä manuaalisesti **$NaturaReverseCharge**-yhdistämismäärityksen laskennallisen kentän **Sähköinen raportointi** -moduulissa.
>
> Muihin sijainteihin liittyvät ohjeet ovat omaa maata tai aluetta koskevissa aloittamisen ohjeissa.

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>Tuo mallin määrityksen konfiguraatioita sähköisestä raportoinnista

1. Valitse RCS:ssä **Sähköinen raportointi** -työtila.
2. Valitse **Microsoft**-määrityspalveluiden luettelosta **Säilöt**.
3. Valitse **Yleiset** ja valitse toimintoruudusta **Avaa**.
4. Tuo mallimääritysten konfiguraatiot seuraavan taulun mukaan toiminnon nimen mukaan.

| Toiminnon nimi                         | Mallin yhdistämismääritys |
|--------------------------------------|-----------------------------|
| Itävallan sähköiset laskut (AT)    | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Belgian sähköinen lasku (BE)      | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Brasilian NF-e (BR)                  | <p>Myyntilaskun kontekstimalli</p><p>Veroasiakirjat</p><p>Vastaussanomamalli</p> |
| Brasilian NFS-e ABRASF Curitiba (BR) | <p>Myyntilaskun kontekstimalli</p><p>Veroasiakirjat</p><p>Vastaussanomamalli</p> |
| Tanskan sähköinen lasku (DK)       | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Egyptin sähköinen lasku (EG)     | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p><p>Vastaussanomamalli</p> |
| Viron sähköinen lasku (EE)     | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Suomen sähköinen lasku (FI)       | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Ranskan sähköinen lasku (FR)       | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Saksan sähköinen lasku (DE)       | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| FatturaPA (IT)                       | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Meksikon CFDI Interfactura (MX)       | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p><p>Vastaussanomamalli</p> |
| Alankomaiden sähköinen lasku (NL)        | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Norjan sähköinen lasku (NO)    | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Espanjan sähköinen lasku (ES)      | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Sähköinen PEPPOL-lasku            | <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |
| Saudi-Arabian sähköinen lasku (SA)| <p>Myyntilaskun kontekstimalli</p><p>Laskumalli</p> |


## <a name="configure-the-application-setup"></a>Määritä sovellusasetukset

1. Valitse luomasi Sähköinen laskutus -toiminto.
2. Valitse **Asetukset** -välilehdessä **Sovelluksen asetukset**.
3. Valitse **Yhdistä sovellus** -kentässä yhteys, joka liittyy Financen tai Supply Chain Managementin esiintymään.
4. Valitse **Sähköisen asiakirjan tyypit** -osassa **Lisää**.
5. Valitse ja määritä **Taulun nimi** -arvo seuraavan taulukon mukaisesti.

    | Toiminnon nimi                         | Yritysasiakirja | Taulun nimi |
    |--------------------------------------|-------------------|------------|
    | Itävallan sähköiset laskut (AT)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Belgian sähköinen lasku (BE)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Brasilian NF-e (BR)                  | <p>Veroasiakirja</p><p>Oikaisukirje</p> | Veroasiakirja |
    | Brasilian NFS-e ABRASF Curitiba (BR) | Palvelun veroasiakirja | Veroasiakirja |
    | Tanskan sähköinen lasku (DK)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Egyptin sähköinen lasku (EG)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Viron sähköinen lasku (EE)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Suomen sähköinen lasku (FI)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Ranskan sähköinen lasku (FR)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Saksan sähköinen lasku (DE)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | FatturaPA (IT)                       | <p>Myyntilasku</p><p>Projektilasku | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Meksikon CFDI Interfactura (MX)       | <p>Myyntilasku</p><p>Pakkausluettelo</p><p>Varastosiirto</p><p>Maksun täydennys</p> | Myyntilaskukirjauskansio |
    | Alankomaiden sähköinen lasku (NL)        | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Norjan sähköinen lasku (NO)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Espanjan sähköinen lasku (ES)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektilasku</p> |
    | Sähköinen PEPPOL-lasku            | <p>Myyntilasku</p><p>Projektin lasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektin lasku</p> |
    | Saudi-Arabian sähköinen lasku (SA)| <p>Myyntilasku</p><p>Projektin lasku</p> | <p>Myyntilaskukirjauskansio</p><p>Projektin lasku</p> |

6. Valitse ja määritä kontekstiarvo seuraavan taulukon mukaisesti kuellekin luodulle taulukon nimelle.

    | Toiminnon nimi                         | Yritysasiakirja | Konteksti |
    |--------------------------------------|-------------------|---------|
    | Itävallan sähköiset laskut (AT)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Belgian sähköinen lasku (BE)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Brasilian NF-e (BR)                  | <p>Veroasiakirja</p><p>Oikaisukirje</p> | <p>Myyntilaskun kontekstimalli – veroasiakirjan konteksti</p><p>Myyntilaskun kontekstimalli – veroasiakirjan oikaisukirjeen konteksti</p> |
    | Brasilian NFS-e ABRASF Curitiba (BR) | Palvelun veroasiakirja| Myyntilaskun kontekstimalli – veroasiakirjan konteksti |
    | Tanskan sähköinen lasku (DK)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Egyptin sähköinen lasku (EG)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Viron sähköinen lasku (EE)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Suomen sähköinen lasku (FI)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Ranskan sähköinen lasku (FR)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Saksan sähköinen lasku (DE)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | FatturaPA (IT)                       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Meksikon CFDI Interfactura (MX)       | <p>Myyntilasku</p><p>Pakkausluettelo</p><p>Varastosiirto</p><p>Maksun täydennys</p> | Myyntilaskun kontekstimalli – myyntilaskun konteksti |
    | Alankomaiden sähköinen lasku (NL)        | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Norjan sähköinen lasku (NO)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Espanjan sähköinen lasku (ES)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Sähköinen PEPPOL-lasku            | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |
    | Saudi-Arabian sähköinen lasku (SA)| <p>Myyntilasku</p><p>Projektin lasku</p> | <p>Myyntilaskun kontekstimalli – myyntilaskun konteksti</p><p>Myyntilaskun kontekstimalli – projektilaskun konteksti</p> |

7. Valitse ja määritä jokaiselle taulukon nimelle ja kontekstille liiketoimintatiedoston määrityksen arvo seuraavan taulukon mukaisesti.

    | Toiminnon nimi                         | Yritysasiakirja | Liiketoiminta-asiakirjan yhdistämismääritys |
    |--------------------------------------|-------------------|---------------------------|
    | Itävallan sähköiset laskut (AT)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Belgian sähköinen lasku (BE)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Brasilian NF-e (BR)                  | <p>Veroasiakirja</p><p>Oikaisukirje</p> | <p>Veroasiakirjan määritys – veroasiakirjan määritys</p><p>Veroasiakirjan määritys – oikaisukirjeen määritys</p> |
    | Brasilian NFS-e ABRASF Curitiba (BR) | Palvelun veroasiakirja | Veroasiakirjan määritys – veroasiakirjan määritys |
    | Tanskan sähköinen lasku (DK)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Egyptin sähköinen lasku (EG)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Viron sähköinen lasku (EE)     | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Suomen sähköinen lasku (FI)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Ranskan sähköinen lasku (FR)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Saksan sähköinen lasku (DE)       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | FatturaPA (IT)                       | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Meksikon CFDI Interfactura (MX)       | <p>Myyntilasku</p><p>Pakkausluettelo</p><p>Varastosiirto</p><p>Maksun täydennys</p> | Laskumallin määritys – Myyntilasku |
    | Alankomaiden sähköinen lasku (NL)        | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Norjan sähköinen lasku (NO)    | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Espanjan sähköinen lasku (ES)      | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Sähköinen PEPPOL-lasku            | <p>Myyntilasku</p><p>Projektilasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |
    | Saudi-Arabian sähköinen lasku (SA)| <p>Myyntilasku</p><p>Projektin lasku</p> | <p>Laskumallin määritys – Myyntilasku</p><p>Laskumallin määritys – projektilasku</p> |


## <a name="country-specific-configuration-of-application-setup"></a>Sovellusasetusten maa-/aluekohtainen konfigurointi

Maan tai alueen mukaan sovellusasetukset saattavat edellyttää tiettyjä konfiguraatiota. 

Yksityiskohtaiset vaiheet ovat maasi tai alueesi käytettävissä olenassa aloitusdokumentaatiossa.

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>Sähköisen laskutuksen toiminnon käyttöönotto palveluympäristössä

1. Valitse **Versiot**-välilehdestä se sähköisen laskutuksen toiminnon versio, jonka haluat ottaa käyttöön.
2. Valitse **Muutoksen tila** \> **Viimeistele**.
3. Valitse **Muuta tilaa** \> **Julkaise**.
4. Valitse **Ota käyttöön**.
5. Määritä **Ota käyttöön yhdistetyssä sovelluksessa** -asetuksen arvoksi **Ei**.
6. Määritä **Ota käyttöön palveluympäristössä** -asetuksen arvoksi **Kyllä**.
7. Valitse **Palveluympäristö**-kentästä sähköinen laskutuksen ympäristö, jossa haluat ottaa sähköisen laskutuksen ominaisuuden käyttöön.
8. Valitse **Päivämäärästä**-kentässä päivämäärä, jolloin sähköisen laskutuksen ominaisuuden tulee olla voimassa sähköisessä laskutuksessa.
9. Valitse **OK**.

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>Sähköisen laskutuksen toiminnon käyttöönotto yhdistetyssä sovelluksessa

1. Valitse **Versiot**-välilehdestä se sähköisen laskutuksen toiminnon versio, jonka haluat ottaa käyttöön.
2. Valitse **Ota käyttöön**.
3. Määritä **Ota käyttöön yhdistetyssä sovelluksessa** -asetuksen arvoksi **Kyllä**.
4. Valitse **Yhdistä sovellus** -kentässä yhteys, joka liittyy Financen tai Supply Chain Managementin esiintymään.
5. Määritä **Ota käyttöön palveluympäristössä** -asetuksen arvoksi **Ei**.
6. Valitse **OK**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Sähköisen laskutuksen ominaisuuden käyttöönotto Financessa tai Supply Chain Managementissa

1. Kirjaudu sisään Financeen tai Supply Chain Managementiin ja varmista, että olet oikeassa yrityksessä.
2. Siirry kohtaan **Organisaation hallinta** \> **Määritys** \> **Sähköisten asiakirjojen parametrit**.
3. Valitse **Ominaisuudet**-välilehdestä maa-/aluekohtainen toiminto, kun haluat ottaa sähköisen laskutuksen käyttöön Financessa tai Supply Chain Managementissa. Seuraavassa taulukossa on luettelo tietyissä maissa / tietyillä alueilla käytettävissä olevista sähköisistä laskutusominaisuuksista. 

    | Toiminnon nimi                                          | Maa tai alue  |
    |-------------------------------------------------------|-----------------|
    | Itävallan sähköiset laskut (AT)                     | Itävalta         |
    | Belgian sähköinen lasku (BE)                       | Belgia         |
    | CFDI – Meksikon sähköinen lasku (MX)                  | Meksiko          |
    | Tanskan sähköinen lasku (DK)                        | Tanska         |
    | Alankomaiden sähköinen lasku (NL)                         | Alankomaat |
    | Egyptin sähköinen lasku (EG)                      | Egypti           |
    | Viron sähköinen lasku (EE)                      | Viro         |
    | Suomen sähköinen lasku (FI)                       | Suomi         |
    | Ranskan sähköinen lasku (FR)                        | Ranska          |
    | Saksan sähköinen lasku (DE)                        | Saksa         |
    | Italian sähköinen lasku (IT)                       | Italia           |
    | NF-e Federal – Brasilian sähköinen lasku (BR)      | Brasilia          |
    | NFS-e – Brasilian kaupungin sähköinen lasku   | Brasilia          |
    | Norjan sähköinen lasku (NO)                     | Norja          |
    | Sähköinen PEPPOL-lasku                             | Yleinen          |
    | Espanjan sähköinen lasku (ES)                       | Espanja           |
    | Saudi-Arabian sähköinen lasku (SA)                 | Saudi-Arabia    |
    

4. Valitse **Tallenna**.

## <a name="issue-electronic-invoices"></a>Sähköisten laskujen lähettäminen

1. Siirry kohtaan **Organisaation hallinta** \> **Säännölliset** \> **Sähköiset asiakirjat** \> **Lähetä sähköisiä asiakirjoja**.
2. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.
3. Lisää kyselysuodattimeen taulun nimi valitsemalla **Lisää**.
4. Valitse taulu, joka sisältää laskut.

    > [!NOTE]
    > Taulun nimen on oltava aiemmin tässä ohjeaiheessa [Määritä sovellusasetukset](#configure-the-application-setup) -osassa olevassa taulussa.

5. Valitse taulusta kentän nimi, johon haluat kohdistaa kyselyn.
6. Kirjoita kyselyn ehdoille taulun nimi ja kentän nimi.
7. Lisää kyselyyn kenttiä ja ehtoja toistamalla vaiheita 5 ja 6 ja valitse sitten **OK**.
8. Valitse **OK**.

## <a name="view-submission-logs"></a>Lähetyslokien tarkasteleminen

1. Siirry kohtaan **Organisaation hallinta** \> **Säännölliset** \> **Sähköiset asiakirjat** \> **Sähköisen asiakirjan lähetysloki**.
2. Valitse **Asiakirjatyyppi**-kentässä taulukko, joka sisältää laskut.

    > [!NOTE]
    > Taulun nimen on oltava aiemmin tässä ohjeaiheessa [Määritä sovellusasetukset](#configure-the-application-setup) -osassa olevassa taulussa.

3. Valitse lasku ruudukosta ja valitse sitten **Kysely** \> **Lähetystiedot**.

## <a name="download-an-electronic-document-file"></a>Sähköisen asiakirjatiedoston lataaminen

1. Siirry kohtaan **Organisaation hallinta** \> **Säännölliset** \> **Sähköiset asiakirjat** \> **Sähköisen asiakirjan lähetysloki**.
2. Valitse **Asiakirjatyyppi**-kentässä taulukko, joka sisältää laskut.
3. Valitse ensin asiakirja ruudukossa ja sitten **Sähköinen asiakirja** \> **Lataa tiedosto**. Sähköisen asiakirjatiedoston sisältävän arkiston lataamista ehdotetaan.

> [!NOTE]
> Ennen kuin tiedostoja voidaan ladata, **Vie tulokset** -vaihtoehto on otettava käyttöön liittyvässä toiminnossa RCS:n sähköisessä laskutustoiminnossa.

## <a name="related-topics"></a>Liittyvät aiheet

- [Sähköisen laskutuksen yleiskatsaus](e-invoicing-service-overview.md)
- [Sähköisen laskutuksen palvelun hallinnan aloittaminen](e-invoicing-get-started-service-administration.md)
- [Brasilian sähköisen laskutuksen käytön aloittaminen](e-invoicing-bra-get-started.md)
- [Meksikon sähköisen laskutuksen käytön aloittaminen](e-invoicing-mex-get-started.md)
- [Italian sähköisen laskutuksen käytön aloittaminen](e-invoicing-ita-get-started.md)
- [Asiakkaiden sähköiset laskut Egyptissä](emea-egy-e-invoices.md)
- [Asiakkaiden sähköiset laskut Saudi-Arabiassa](emea-sau-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
