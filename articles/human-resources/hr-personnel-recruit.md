---
title: Ehdokkaiden työhönotto
description: Tässä aiheessa kerrotaan, miten ehdokkaiden työhönotto tehdään Dynamics 365 Human Resources -sovelluksessa.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669165"
---
# <a name="recruit-job-candidates"></a>Ehdokkaiden työhönotto

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources auttaa työhönottopyyntöjen hallinnassa. Sen avulla myös ehdokkaiden siirtäminen työntenkijöiksi sujuu saumattomasti. Jos organisaatiossa käytetään erillistä työhönottosovellusta, työhönottoprosessissa saatetaan suorittaa seuraavat vaiheet:

- Syötä rekrytointipyyntö Human Resources -sovelluksessa.
- Vastaanota ehdokkaiden suositukset työhönottosovelluksesta Human Resourcesiin.
- Tee ehdokkaan hyväksymisprosessi valmiiksi Human Resourcesissa.

Jos käytössä ei ole erillistä työhönottosovellusta, voit hallinnoida ehdokkaita Human Resourcesissa myös manuaalisesti.

>[!NOTE]
>Jos olet järjestelmänvalvoja tai kehittäjä ja haluat integroida Human Resourcen kolmannen osapuolen työhönottosovellukseen, katso lisätietoja kohdasta [Common Data Service -integroinnin määrittäminen](hr-admin-integration-common-data-service.md) ja [Common Data Servicen virtuaalientiteettien määrittäminen](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Voit myös etsiä työhönoton integrointisovelluksia [AppSourcesta](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
> Saat lisätietoja LinkedIn Talent Hub -integroinnin esiversiotoiminnosta kohdasta [LinkedIn Talent Hub -integrointi](hr-admin-integration-linkedin.md).

## <a name="enable-recruiting-requests"></a>Ota työhönottopyynnöt käyttöön

Jos hlauat lähettää työhönottopyyntöjä Human Resourcesissa, ota ensin toiminto käyttöön **Human resources -parametreissa**.

1. Valitse **Henkilöstön hallinta** -työtilassa **Linkit**.

2. Valitse **Määritys**-kohdasta **Henkilöstöparametrit**.

3. Määritä **Yleistiedot**-välilehden **TYÖHÖNOTTO**-kohdan **Ota työhönottopyynnöt käyttöön** -arvoksi **Kyllä**.

   ![Ota työhönottopyynnöt käyttöön](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a>Työhönottopyynnön sijainnin lisääminen

Voit lisätä organisaation mahdolliset useat sijainnit, jotta pyytäjät voivat uuden valita rekrytoitavan henkilön työskentelysijainnin. Sijainti sisällytetään työpaikkailmoitukseen.

1. Syötä hakupalkkiin **työhönottopyynnön sijainti**.

2. Valitse **Uusi**.

3. Syötä **Työhönottopyynnön sijainti** -kenttään sijainnin nimi.

   ![Työhönottopyynnön sijainnin lisääminen](./media/hr-recruit-0a-add-location.png)

4. Syötä **Kuvaus**-kohtaan sijainnin kuvaus.

5. Valitse **Sijainti**-kohdassa **Lisää**. Jos **Uusi osoite** -ponnahdusikkuna tulee näkyviin, syötä sijainnin osoite.

   ![Anna osoite](./media/hr-recruit-0b-address.png)

6. Syötä **Yhteyshenkilön tiedot** -kohtaan sijainnin yhtyshenkilön tiedot.

7. Valitse **Tallenna**.

## <a name="add-a-recruiting-request"></a>Työhönottopyynnön lisääminen

Esimiehet voivat lähettää työhönottopyyntöjä Human Resourcesissa. Jos käytät erillistä työhönottosovellusta, näiden vaiheiden suorittaminen lähettää työhönottopyynnön ja aloittaa työhönottoprosessin kyseisessä sovelluksessa. Muussa tapauksessa voit aloittaa oman sisäisen työhönotoprosessin työnkulun tämän menetelmän avulla.

1. Valitse **Työntekijän itsepalvelu**.

2. Valitse **Oma ryhmä** -välilehti.

3. Valitse **Työhönottopyyntö**.

   ![Työhönottopyynnön aloittaminen](./media/hr-recruit-1-request-to-recruit.png)

4. Täytä **Kuvaus**-, **Työ**- ja **Arvioitu alkamispäivämäärä** -kentät.

   ![Työhönottopyynnön suorittaminen](./media/hr-recruit-2-request-to-recruit.png)

5. Valitse **Jatka**. Sijainnin työhönottopyyntö tulee näkyviin.

6. Valitse **Yleistiedot**-kohtaan työhönottaja avattavasta **Työhönottaja**-luettelosta. Valitse sitten sijainti avattavasta **Työhönottopyynnön sijainti** -luettelosta.

7. Muuta **Työ**-kohdassa tarvittavat tiedot ja valitse **Luo tiedot työstä**.

   ![Luo tiedot työstä](./media/hr-recruit-3-create-details-from-job.png)

   Muut työhönottopyynnön kentät täytetään käyttämällä annetun työn oletustietoja.

8. Syötä **Ulkoinen kuvaus** -kenttään ulkoisen työn kuvaus.

9. Valitse **Toimet**-kohdassa **Lisää** ja valitse tämän työhönottopyynnön toimi.

   ![Toimen lisääminen](./media/hr-recruit-4-select-position.png)

10. Valitse **Taidot**-kentässä **Lisää** ja valitse sitten taito.

11. Valitse **Koulutusvaatimukset** -kohdassa **Lisää** ja valitse sitten avattavat **Koulutus**- ja **Koulutustaso**-luettelot.

   ![Lisävaatimusten lisääminen](./media/hr-recruit-5-select-educational-requirements.png)

12. Lisää **Kommentti**-kohtaan tarvittavat kommentit.

13. Valitse **Kompensaatio**-kohdassa taso avattavasta **Taso**-luettelosta. Muuta sitten tarvittaessa **Alaraja**-, **Tarkistuspiste**- ja **Yläraja**-kohtaa.

14. Kun työhönottopyyntö on valmis ja haluat aloittaa työhönottoprosessin, valitse valikkorivillä **Aktivoi**.

   ![Työhönottopyynnön aktivoiminen](./media/hr-recruit-6-activate-recruit-request.png)

15. Valitse **Tallenna**.

## <a name="view-and-edit-your-recruiting-requests"></a>Työhönottopyyntöjen tarkasteleminen ja muokkaaminen

Tee seuraavasti, jos olet esimies ja haluat tarkastella omia pyyntöäsi:

1. Valitse **Työntekijän itsepalvelu**.

2. Valitse **Oma ryhmä** -välilehti.

3. Valitse **Oman ryhmän tiedot** -kohdan **Työhönottopyynnöt**-välilehti.

   ![Valitse Työhönottopyynnöt-välilehti](./media/hr-recruit-7-recruiting-requests.png)

4. Voit tarkastella tai muokata työhönottopyyntöä valitsemalla sen ruudukosta.

Tee seuraavasti, jos olet HR-ammattilainen ja haluat tarkastella kaikkia työhönottopyyntöjä:

1. Valitse **Henkilöstöhallinto**.

2. Valitse **Työhönottopyynnöt**.

   ![Työhönottopyyntöjen tarkasteleminen henkilöstöhallinnossa](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Voit tarkastella tai muokata työhönottopyyntöä valitsemalla sen ruudukosta.

## <a name="add-or-edit-a-candidate-profile"></a>Ehdokasprofiilin lisääminen tai muokkaaminen

Jos organisaatio on integroitu toiseen sovellukseen työhönottopyyntöjen hallintaa varten, työhönottopyynnöt lähetetään edelleen tähän sovellukseen. Työhönottosovellus lähettää tämän jälkeen ehdokkaan tiedot takaisin Human Resourcesiin. Muussa tapauksessa voit seurata omia sisäisiä työhönottoprosesseja ja syöttää ehdokkaan tiedot manuaalisesti.

1. Valitse **Henkilöstöhallinto**.

2. Valitse **Linkit**.

3. Valitse **Työhönotto**-kohdassa **Ehdokkaat**.

   ![Ehdokkaiden tarkasteleminen](./media/hr-recruit-9-candidates.png)

4. Voit lisätä ehdokkaan valitsemalla **Uusi**. Jos haluat muokata aiemmin luotua ehdokasta, valitse ehdokas luettelosta ja valitse sitten **Muokkaa**. Ehdokasprofiili tulee näkyviin.

5. Syötä **Ehdokkaan yhteenveto** -kohtaan ehdokkaan tiedot tai muokkaa niitä.

6. **Valitse työhönottopyyntö** -kohdassa työhönottopyyntö, johon ehdokas linkitetään. Täytä sitten soveltuvat **Arvioitu aloituspäivämäärä**-, **Työhön ottava esimies**-, **Toimi**- ja **Kuvaus**-kentät.

   ![Työhönottopyynnön linkki](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Täytä kaikki ne seuraavien alueiden tiedot, jotka haluat sisällyttää ehdokkaan tietueeseen:
   - **Huomautukset**
   - **Ammattikokemus**
   - **Yhteystiedot**
   - **Koulutus**
   - **Osaamisalueet**
   - **Todistukset**
   - **Seulonnat**

8. Valitse **Tallenna**.

## <a name="hire-a-candidate"></a>Ehdokkaan työhönotto

Kun olet valmis ehdokkaan työhönottoa varten, siirrä ehdokas työntekijäksi seuraavasti.

1. Valitse ehdokkaan lomakkeesta **Työhönotto**.

   ![Ehdokkaan työhönotto](./media/hr-recruit-11-hire.png)

2. Täytä kaikki kentät **Palkkaa uusi työntekijä** -lomakkeen **Tiedot**-kohdassa.

   ![Uuden työntekijän tietojen syöttäminen](./media/hr-recruit-12-hire-new-worker.png)

3. Tarkista **Position tiedot** -kohdan tiedot ja muuta niitä tarvittaessa.

4. Valitse **Perehdytyksen tarkistusluettelot** -kohdassa kyseisen työntekijän asiaankuuluvat perehdytyksen tarkistusluettelot.

5. Valitse **Jatka**, jos haluat luoda työntekijätietueen.

   >[!NOTE]
   >Organisaation työnkuluista riippuen ehdokkaan tietue voi siirtyä lisähyväksyntävaiheisiin ennen työntekijätietueeksi muuttamista.

## <a name="decide-not-to-hire-a-candidate"></a>Päätös olla ottamatta ehdokasta töihin

Jos päätät olla ottamatta ehdokasta töihin, noudata näitä toimintoja ja poista tämä ennakkotarkistusprosessista. 

1. Valitse ehdokkaan lomakkeessa **Älä ota töihin** -kohta.

   ![Ehdokkaan työhönoton peruminen](./media/hr-recruit-13-do-not-hire.png)

2. Valitse **Syykoodi** ja lisää mahdolliset kommentit.

3. Valitse **OK**.

## <a name="dismiss-a-candidate"></a>Ehdokkaan hylkääminen

Tarvittaessa voit hylätä ehdokkaan työhönoton jälkeen. Ehdokas voi esimerkiksi hylätä tarjouksen tai jättää tulematta töihin ensimmäisenä päivänä.

- Valitse ehdokkaan lomakkeessa **Hylkää ehdokas** -kohta.

  ![Hylkää ehdokas](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Lisätietoja

[Common Data Service -virtuaaliyksiköiden määrittäminen](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Työvoimasi organisointi](hr-personnel-departments-jobs-positions.md)<br>
[Työn komponenttien määrittäminen](hr-personnel-jobs.md)