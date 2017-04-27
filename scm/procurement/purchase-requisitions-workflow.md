---
title: "ostoehdotuksen työnkulku"
description: "Työnkulkuprosessi siirtää ostoehdotuksia tarkistusprosessissa eteenpäin alkuperäisestä Luonnos-tilasta lopulliseen Hyväksytty-tilaan. Kun hankintapyyntö lähetetään tarkastettavaksi, työnkulkuprosessi alkaa. Sen jälkeen kun hankintapyyntö on hyväksytty, ostotilaus voidaan kehittää hankintapyyntöriveille ja lähettää toimittajalle, jotta tilaus voidaan toteuttaa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 7c5986dbce88a1cb704dddfc2afbcf2ac8c4b0dd
ms.lasthandoff: 03/31/2017


---

# <a name="purchase-requisition-workflow"></a>ostoehdotuksen työnkulku

[!include[banner](../includes/banner.md)]


Työnkulkuprosessi siirtää ostoehdotuksia tarkistusprosessissa eteenpäin alkuperäisestä Luonnos-tilasta lopulliseen Hyväksytty-tilaan. Kun hankintapyyntö lähetetään tarkastettavaksi, työnkulkuprosessi alkaa. Sen jälkeen kun hankintapyyntö on hyväksytty, ostotilaus voidaan kehittää hankintapyyntöriveille ja lähettää toimittajalle, jotta tilaus voidaan toteuttaa.

Ennen kuin ostoehdotus voidaan lähettää tarkastettavaksi, työnkulku pitää määrittää. Työnkulkuprosessi voi sisältää yhden tai useamman tarkastusvaiheen missä tahansa järjestyksessä. Työnkulkuprosessi voidaan myös määrittää ohittamaan tarkastustehtävät ja hyväksymään hankintapyynnön automaattisesti. Voit määrittää työnkulun reitittämään ostoehdotuksen yhtenä asiakirjana tai reitittää yksittäiset ostopyyntörivit oikeille tarkistajille. Voit myös luoda skenaarion, jossa ostoehdotus reititetään yhtenä asiakirjana joillekuille tarkastajille ja valitut ostopyyntörivit reititetään muille tarkastajille.  

Jos ostoehdotusrivit tarkistetaan yksitellen, arviointiprosessin on täytettävä kaikki ostoehdotusrivit, ennen kuin työnkulkuprosessi voi siirtyä seuraavaan vaiheeseen ja ennen kuin hankintaehdotuksen arvosteluprosessi voidaan kokonaisuudessaan suorittaa. Kun ostoehdotuksen ja sen kaikkien rivien tarkastusprosessi on valmistunut, ostoehdotuksen yleiseksi tilaksi päivitetään **Hyväksytty**.  

Voit määrittää työnkulkusi kuvaamaan hankintapyyntöjen työprosessia omassa organisaatiossasi. Kun määrität ostoehdotusten työnkulkuprosessia, ota huomioon seuraavat seikat:

-   Mitkä menot pitää tarkistaa?
-   Mitkä menot voidaan hyväksyä automaattisesti?
-   Kenen tulee tarkistaa ja hyväksyä hankintapyynnöt? Missä roolissa nämä käyttäjät ovat?
-   Mitä prosessia on noudatettava, jos tarkistaja ei ole käytettävissä?

Seuraavat esimerkit kuvaavat kahta tapaa määrittää ostoehdotusten työnkulku.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>Esimerkki 1: Lähetä hankintapyyntö yksittäisenä asiakirjana tarkastettavaksi.
Seuraava esimerkki näyttää kuinka hankintapyyntö voi mennä työnkulun tarkastusprosessin läpi yksittäisenä asiakirjana. Ostoehdotuksen rivejä ei reititetä yksittäin. Tässä esimerkissä, seuraavat roolit sisältyvät työnkulkuun:

-   **Pyytäjä** – käyttäjä, joka pyytää nimikkeitä tai palveluja. Pyytäjä voi valmistella hankintapyynnön tai joku muu työntekijä voi valmistella sen hänen puolestaan. Tämä työntekijä on valmistelija. Valmistelija on vastuussa hankintapyynnön käsittelemisestä koko tarkistusprosessin ajan. Hankintaehdotuksien valmistelija on ainoa, joka voi muokata sitä.

**Huomautus:** Työntekijälle tulee antaa tarvittavat oikeudet luoda ostoehdotus jonkun toisen puolesta. Voit määrittää oikeudet **Hankintapyyntöoikeus**-sivulla.

-   **Hankintaedustaja** – käyttäjä, joka tekee hankintatarkistuksen ja voi hyväksyä asiakirjan.
-   **Pyytäjän esimies** – käyttäjä, joka tekee johtotason tarkistuksen ja voi hyväksyä asiakirjan.

![Ostoehdotustyönkulun tarkasteluprosessi](./media/purchreqworkflowoverview_submission.gif)  
Tässä esimerkissä hankintapyyntöjen työnkulkuprosessi sisältää seuraavat vaiheet:

1.  Valmistelija lähettää hankintapyynnön tarkistettavaksi.
2.  Hankintaedustaja vastaanottaa ilmoituksen. Ilmoituksessa jossa pyydetään hankintaedustajaa vahvistamaan ostoehdotuksen tiedot. Jos tarvittavia tietoja puuttuu, hankintaedustaja voi lisätä tiedot tai lähettää ostoehdotuksen takaisin valmistelijalle, joka lisää ne. Kun tarvittavat kentät on täytetty, ostoehdotus voidaan siirtää tarkastusprosessin seuraavaan vaiheeseen.
3.  Pyytäjän esimies tarkistaa hankintapyynnön. Ostoehdotus voidaan reitittää pyytäjän esimiehelle, jos esimerkiksi ostoehdotuksen summa ylittää pyytäjän ostoehdotuksia koskevan kulutusrajan. Pyytäjän esimies voi hyväksyä tai hylätä hankintapyynnön tai lähettää sen takaisin valmistelijalle, joka tekee muutokset.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>Esimerkki 2: Lähetä yksittäiset hankintapyyntörivit tarkastettavaksi
Seuraava esimerkki osoittaa, kuinka yksittäiset ostoehdotusrivit voidaan reitittää työnkulun läpi. Jokaisen yksittäisen rivin prosessi on yleisesti ottaen sama kuin ostoehdotusprosessi, jossa ostoehdotus tarkistetaan yksittäisenä asiakirjana. Työnkulkuprosessi on kuitenkin suoritettava jokaiselle riville yksitellen, ennen kuin työnkulku voidaan suorittaa loppuun koko ostoehdotukselle.  

Tässä esimerkissä työntekijä tekee ehdotuksen julisteista ja T-paidoista markkinointikampanjaa varten. Julisteiden maksaminen jaetaan markkinointiosaston ja myyntiosaston kesken. Jos julisteiden ja T-paitojen kustannukset ylittävät osastopäälliköiden nimenkirjoitusrajan, myös ryhmän esimiehen on tarkistettava ostoehdotus.  

Tässä esimerkissä, seuraavat roolit sisältyvät työnkulkuun:

-   **Pyytäjä** – käyttäjä, joka pyytää nimikkeitä tai palveluja. Pyytäjä voi valmistella hankintapyynnön tai joku muu työntekijä voi valmistella sen hänen puolestaan. Tämä työntekijä on valmistelija. Valmistelija on vastuussa hankintapyynnön käsittelemisestä koko tarkistusprosessin ajan. Hankintaehdotuksien valmistelija on ainoa, joka voi muokata sitä.

**Huomautus:** Työntekijälle tulee antaa tarvittavat oikeudet luoda ostoehdotus jonkun toisen puolesta. Voit määrittää oikeudet **Hankintapyyntöoikeus**-sivulla.

-   **Hankintaedustaja** – käyttäjä, joka tekee hankintatarkistuksen ja voi hyväksyä asiakirjan.
-   **Pyytäjän esimies** – käyttäjä, joka tekee johtotason tarkistuksen ja voi hyväksyä asiakirjan.
-   **Osaston esimies** – käyttäjä, joka tekee menojen tarkistuksen ja voi hyväksyä asiakirjan.
-   **Ryhmän esimies** – käyttäjä, jolla on nimenkirjoitusoikeus tarkistuksessa ja joka voi hyväksyä asiakirjan.

![Ostoehdotusrivin työnkulun tarkasteluprosessi](./media/purchreqlineworkflowoverview.gif)  
Tässä esimerkissä hankintapyyntölinjojen työnkulkuprosessi sisältää seuraavat vaiheet:

1.  Valmistelija lähettää hankintapyynnön tarkistettavaksi. Jokainen rivi reititetään tarkistajalle, joka on määrätty vastaanottajaksi työnkulkuprosessissa.
2.  Hankintaedustaja vastaanottaa ilmoituksen. Ilmoituksessa pyydetään hankintaedustajaa vahvistamaan ostoehdotuksen sekä sen rivien tiedot. Kun ostoedustaja avaa ostoehdotuksen, kaikki rivit ovat näkyvissä mutta visuaalinen ilmaisin näyttää, mitkä rivit ostoedustaja on lähettänyt tarkistettavaksi. Jos tarvittavia tietoja puuttuu, hankintaedustaja voi lisätä tiedot tai lähettää ostoehdotusrivin takaisin valmistelijalle, joka lisää ne. Kun tarvittavat kentät on täytetty, ostoehdotusrivi voidaan siirtää tarkastusprosessin seuraavaan vaiheeseen. Ostoehdotusrivit voivat edetä tarkistusprosessin läpi toisistaan riippumatta.
3.  Pyytäjän esimies tarkistaa ja hyväksyy hankintapyyntörivit. Hyväksyntä voidaan reitittää pyytäjän esimiehelle, jos esimerkiksi ostoehdotusrivin summa ylittää pyytäjän ostoehdotusrivejä koskevan kulutusrajan. Esimies voi hyväksyä tai hylätä yhden tai molemmat hankintapyyntörivit.
4.  Markkinointiosaston johtaja tarkistaa sekä julisteita että T-paitoja koskevat ostoehdotusrivit. Myyntiosaston osastonjohtaja tarkistaa hankintapyyntörivin ainoastaan julisteille, koska se on ainoa meno johon veloitetaan myyntiosastolta.
5.  Ryhmän esimies tarkistaa ja hyväksyy T-paitojen ostoehdotusrivin vain, jos hänen hyväksyntänsä tarvitaan esimerkiksi siksi, että ostoehdotusrivin summa ylittää osastopäällikön hyväksymisrajan. Ryhmän esimiehen ei tarvitse hyväksyä hankintapyyntöriviä julisteille.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Ostoehdotusten työnkulun määrittäminen
Lähettääksesi hankintapyynnön tarkistettavaksi, sinun tulee määrittää hankintapyynnön työnkulkuprosessi. Määrittelemäsi työnkulkuprosessi ohjaa vuorovaikutusta käyttäjän, joka pyysi artikkeleita (pyytäjä) ja työnkulun tarkastajan sekä hyväksyjän välillä. Ostoehdotuksen reititys riippuu työnkulun konfiguraatiossa määritetyistä ehdoista. Nämä ehdot määrittävät esimerkiksi, milloin ostoehdotus määritetään, reitityksen kohteena olevan käyttäjän tai roolin sekä toiminnot, joita käyttäjät voivat suorittaa.  

Tämän aiheen esimerkit näyttävät, kuinka ostoehdotus voidaan reitittää työnkulun läpi yksittäisenä asiakirjana tai yksittäisinä ostoehdotusriveinä. Voit myös määrittää ostoehdotusten työnkulun, joka kuvaa organisaatiosi sisäistä ostoehdotusten tarkastusta.  

Osallistujat tai tarkistajat, joille tehtävä määritetään työnkulussa, voivat olla tietyn käyttäjäryhmän jäseniä, käyttäjiä, joilla on tietty käyttöoikeusrooli, käyttäjiä, jotka on liitetty lähettäjän kanssa esimieshierarkiaan tai nimettyjä käyttäjiä tai käyttäjiä, joilla on tietyt menovastuualueet.

### <a name="purchase-requisition-expenditure-reviewers"></a>Ostoehdotuksen kulujen tarkistajat

Voit asettaa menojen tarkistajan määritykset reitittämään dynaamisesti menot tarkastettavaksi projektirooliin määritetyn käyttäjän tai sen taloushallinnon dimension mukaan, johon meno kirjataan kuluksi. Työnkulkuprosessi määrittää tietyn projektin roolin tai taloushallinnon dimension omistajan avulla, kenelle menot reititetään.  

Voit määrittää yhden tai useamman menojen tarkistajan määrityksen ja valita määrityksen, kun luot työnkulun. Voit määrittää menojen tarkistajan arvot jokaiselle organisaation oikeussubjektille. Kun olet määrittänyt menojen tarkistajan määritykset, voit liittää määrityksen työnkulkutehtävään.  

Sinun ei tarvitse määrittää menojen tarkistajan määrityksiä. Voit sen sijaan määrittää tietyt käyttäjät tai käyttäjäryhmät tarkistajiksi, kun määrität työnkulun. Jos sinulla on monimutkainen organisaatio, menojen tarkistajat voivat parantaa hyväksyntäprosessin tehokkuutta. Lisäksi jos määrität menojen tarkistajia, sinun ei tarvitse päivittää työnkulun tarkistajamäärityksiä aina, kun tarkistajan työrooli muuttuu.  

Voit määrittää menojen tarkistajat **Ostoehdotuksen kulujen tarkistajat** -sivulla. Luo menojen tarkistajan määritys ja kirjoita kunkin organisaatioon kuuluvan yrityksen arvot. Projektiin liitetyille ehdotuksille voit määrittää roolin, joka vastaa ehdotusten tarkistamisesta: Projektipäällikkö, Projektin budjettipäällikkö tai Projektin myyntipäällikkö. Menot reititetään käyttäjälle, joka on liitetty kyseiseen rooliin. Voit myös reitittää menon taloushallinnon dimension omistajalle valitsemalla sopivan taloushallinnon dimension vaihtoehdon **Organisaation distribuutiot** -välilehdestä.  

Jos haluat käyttää jotakuta työnkulussa määrittämääsi menojen tarkistajaa, määritä **Osallistujan tyyppi** -asetukseksi **Kulujen osallistujat** kyseisen työnkulun elementin ** Toimeksianto**-ominaisuuksissa.

<a name="see-also"></a>Lisätietoja
--------

[Kulutusehdotuksen luominen (tehtävän ohjaus)](https://ax.help.dynamics.com/en/wiki/create-a-requisition-for-consumption/)

[Ostoehdotusten liiketoimintaprosessien työnkulun määrittäminen](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions) (raportti)

[Hankinnan työnkulut](procurement-sourcing-workflows.md)

[Ostoehdotusten yhteenveto](purchase-requisitions-overview.md)




