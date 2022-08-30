---
title: Commerce-keskustelu ja Customer Servicen monikanava -moduuli
description: Tässä artikkelissa kerrotaan Commerce-keskustelu ja Customer Servicen monikanava -moduulista Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: e4a004b929138f0a04c19d6a94278cfad6e83303
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346382"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Commerce-keskustelu ja Customer Servicen monikanava -moduuli

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä artikkelissa kerrotaan *Customer Servicen monikanavan Commerce-keskustelu* -moduulista Microsoft Dynamics 365 Commercessa.

Commerce-moduulikirjastoon on lisätty Commerce-keskustelu ja Customer Servicen monikanava -moduuli Commerse-version 10.0.29 julkaisussa. Commerce-keskustelutoiminto antaa sähköisen kaupankäynnin asiakkaille mahdollisuuden keskustella Dynamics 365 Omnichannel for Customer Service -ratkaisussa. Toiminto sisältää live-asiakaspalvelijan tuen asiakaskyselyjen käsittelemiseksi, asiakaspalvelun ja Commerce-asiakkaiden myynnin edistämisen.

Commerce-keskustelutoiminnon avulla jälleenmyyjät voivat saavuttaa seuraavat tavoitteet:

- henkilökohtaisen yhteydenpidon lisääminen asiakkaiden pitämisen parantamiseksi
- asiakaspalvelun parantaminen ihmisasiakaspalvelijan ja itsepalvelun keskustelubottien integroinnin avulla
- apua asiakaspalvelijoille kokemuksen hankkimiseksi toiminnallisia parannuksia ja aktivointia tarjoavien reaaliaikaisten asiakasprofiilien, tilausten ja ostotietojen avulla
- yleisen asiakastyytyväisyyden parantaminen myynnin kasvattamiseksi.

Seuraavat toiminnot ovat käytettävissä Commerce-keskustelutoiminnon osana:

- Commerce-keskustelu ja Customer Servicen monikanava
- **Commercen puhelinkeskus** sovellusvälilehtenä asiakaspalvelijakokemuksessa Dynamics 365 Omnichannel for Customer Service -ratkaisussa

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Customer Servicen monikanavan edellytykset

Edellytyksenä on määritettävä Customer Servicen monikanavan hallinnan pienoissovelluksen keskustelu ja hankittava joitakin parametreja Commerce-keskustelukokemuksen määrittämiseksi. Lisätietoja on kohdassa [Keskustelukanavan määrittäminen](/dynamics365/customer-service/set-up-chat-widget).

Customer Servicen monikanavan hallinnan pienoissovelluksen keskustelun määrittämisen jälkeen käytettävissä on komentosarja, joka muistuttaa alla olevaa esimerkkiä.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Kopioi tämä komentosarja, koska sen arvoja tarvitaan keskustelumoduulin määrittämisessä.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Commerce-keskustelu ja Customer Servicen monikanava – pakolliset kentät

Seuraavassa taulukossa ovat Customer Servicen monikanavan hallinnan pienoissovelluksen komentosarjan arvo, jotka vaaditaan Commerce-keskustelu ja Customer Servicen monikanava -moduulin määrittämisessä.

| Pienoissovelluksen ominaisuus | Kuvaus |
| ------------- |--------------|
| Komentosarjan lähde | Keskustelupienoissovelluksen komentosarjan **src**-arvo. |
| Tietosovelluksen tunnus | Keskustelupienoissovelluksen komentosarjan **data-app-id**-arvo. |
| Tieto-organisaation tunnus | Keskustelupienoissovelluksen komentosarjan **data-org-id**-arvo. |
| Tieto-organisaation URL-osoite | Keskustelupienoissovelluksen komentosarjan **data-org-url**-arvo. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>Commerce-keskustelukokemuksen määrittäminen sähköisen kaupankäynnin sivustossa

Eräs suositeltava tapa ottaa käyttöön keskustelukokemus sähköisen kaupankäynnin sivustossa on lisätä Commerce-keskustelu ja Customer Servicen monikanava -moduuli sähköisen kaupankäynnin sivuston sivujen jaettuun ylätunnistekatkelmaan.

Voit lisätä keskustelumoduulin sivuston ylätunnistekatkelmaan Commercen sivustonmuodostimessa seuraavasti.

1. Siirry sivuston sivustonmuodostimessa **Katkelmat**-kohtaan.
1. Valitse **Uusi**.
1. Valitse **Valitse katkelma** -valintaikkunassa **Commerce-keskustelu ja Customer Servicen monikanava** -moduulissa, syötä osan nimi ja valitse sitten **OK**.
1. Valitse ääriviivanäkymässä **Msdyn365 cs -keskustelun yhdistin** -paikka.
1. Noudata oikealla olevassa **Keskustelun ominaisuudet** -ruudussa seuraavia ohjeita:

    1. Syötä **Komentosarjan lähde** -kenttään **src**-arvo, joka saatiin Customer Servicen monikanava -komentosarjasta.
    1. Syötä **Tietosovelluksen tunnus** -kenttään **data-app-id**-arvo, joka saatiin Customer Servicen monikanava -komentosarjasta.
    1. Syötä **Tieto-organisaation tunnus** -kenttään **data-org-id**-arvo, joka saatiin Customer Servicen monikanava -komentosarjasta.
    1. Syötä **Tieto-organisaation URL-osoite** -kenttään **data-org-url**-arvo, joka saatiin Customer Servicen monikanava -komentosarjasta.

    ![Commerce-keskustelu-moduulin katkelman luominen Commerce-sivustonmuodostimessa.](media/Commerce-chat-creating-new-fragment.png)

1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.
1. Siirry **Katkelmat**-kohtaan ja avaa ylätunnistekatkelma sivustossa.
1. Valitse **Oletussäilö**-paikassa kolme pistettä (**...**) ja valitse sitten **Lisää katkelma**.
1. Valitse **Valitse moduulit** -valintaikkunassa keskustelukatkelma, jonka loit aiemmin, ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Commerce headquartersin lisääminen sovellusvälilehtenä Customer Servicen monikanavaan

Voit lisätä sovellusvälilehden Commerce headquartersille Customer Servicen monikanavassa. Live-asiakaspalvelijat voivat tämän jälkeen käyttää Customer Servicen monikanavan asiakaspalvelijakokemuksen käyttöliittymää ja käyttää helposti Dynamics 365 Commerce Customer Service -moduulia. Se sisältää kontekstuaalista tietoa asiakkaista ja näiden myyntitilauksista. Lisäksi asiakaspalvelun asiakaspalvelijat voivat tehdä uusia tilauksia, käynnistää palautuksia ja vahvistaa tilaustietoja.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Uuden sovellusvälilehden luominen Commerce headquartersin lataamiseksi iFrame-moduulissa 

Seuraavien ohjeiden avulla voit luoda uuden sovellusvälilehden, joka lataa Commerce headquartersin iFrame-moduulissa.

1. Avaa [Power Apps Maker Portal](https://make.powerapps.com).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sovellukset**.
1. Valitse **asiakaspalvelun hallintakeskus**.
1. Siirry **asiakaspalvelijakokemukseen**.
1. Valitse **Sovellusvälilehtimallit**-kohdassa **Hallitse**.
1. Luo uusi sovellusvälilehti, jonka tyyppi on **Kolmannen osapuolen sivusto**. Lisätietoja on kohdassa [Sovellusvälilehtimallien hallinta](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter).
1. Syötä **Parametrit**-kohdan **Arvo**-kentän **url**-parametriin seuraava URL-osoite, jossa `<YourOrganizationHeadquartersURL>` ja `<LegalEntityname>` korvataan soveltuvilla arvoilla. Monikanavan asiakaspalvelu lukee keskustelukontekstista kohdan **{AccountNumber}**. Älä siis muuta kohtaa **{AccountNumber}**.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. Jätä **data**-parametrin **Arvo**-kenttä tyhjäksi.

![Sovellusvälilehden luominen Dynamics 365 Omnichannel Customer Servicessa.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Uuden sovellusvälilehden käyttöönotto asiakaspalvelijoille Dynamics 365 Omnichannel for Customer Servicessa

Jos haluat ottaa käyttöön uuden sovellusvälilehden asiakaspalvelijoille Dynamics 365 Omnichannel for Customer Servicessa, noudata alla olevia ohjeita.
    
1. Avaa [Power Apps Maker Portal](https://make.powerapps.com).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sovellukset**.
1. Valitse **asiakaspalvelun hallintakeskus**.
1. Siirry kohtaan **Asiakastuki \> Työnkulut**.
1. Avaa asiakaspalvelijoille luotu työnkulku ja valitse **Lisäasetukset**-kohdassa **Istunnon oletusarvot**.
1. Valitse **Sovellusvälilehdet**-kohdassa **Lisää olemassa oleva sovellusvälilehti** ja lisää aiemmin luomasi sovellusvälilehti. Tämä vaihe varmistaa, että Commerce headquartersin iFrame-moduulissa lataava sovellusvälilehti näkyy asiakaspalvelijan vastaanottaessa saapuvan keskustelun sähköisen kaupankäynnin sivustossa.

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Kontekstimuuttujien lisääminen Dynamics 365 Omnichannel for Customer Servicessa

Alla olevien ohjeiden avulla voit lisätä kontekstimuuttujia Dynamics 365 Omnichannel for Customer Servicessa.

1. Avaa [Power Apps Maker Portal](https://make.powerapps.com).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sovellukset**.
1. Valitse **asiakaspalvelun hallintakeskus**.
1. Siirry kohtaan **Asiakastuki \> Työnkulut**.
1. Avaa asiakaspalvelijoille luotu työnkulku ja siirry **Lisäasetukset**-kohdassa **Kontekstimuuttuja**-osaan.
1. Valitse **Muokkaa** ja lisää sitten **AccountNumber** kontekstimuuttujana, jonka tyyppi on **Teksti**. Tämä muuttuja auttaa Commerce headquartersia lataamaan asiakastiedot vastaavien tilinumeroiden kanssa.

> [!NOTE]
> Jos haluat lukea sähköisen kaupankäynnin kanavaan kirjautuneiden käyttäjien sähköpostiosoitteet ja nimet, voit lisätä **AccountNumber**-kontekstimuuttujan lisäksi **Sähköposti**- ja **Nimi**-kohdat kontekstimuuttujina, jonka tyyppi on **Teksti**.
