---
title: ชนิดของปลายทาง ER ใน Power BI
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการกำหนดค่าคอนฟิกชนิดปลายทาง ER ของ Power BI สำหรับเอกสารขาออก
author: NickSelin
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 10.0.09
ms.openlocfilehash: a6b6a2e4bc3c0eca8185f501121d9d1ba1b4e063
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561985"
---
# <a name="power-bi-destination"></a><span data-ttu-id="0a631-103">ปลายทางของ Power BI</span><span class="sxs-lookup"><span data-stu-id="0a631-103">Power BI destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a631-104">คุณสามารถกำหนดค่าคอนฟิกปลายทางของ Microsoft Power BI สำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการกำหนดค่าคอนฟิกให้สร้างเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="0a631-104">You can configure a Microsoft Power BI destination for each folder or file component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="0a631-105">เอกสารที่สร้างขึ้นจะถูกจัดเก็บไว้ในโฟลเดอร์ SharePoint ที่ตั้งค่าคอนฟิกไว้ก่อนหน้านี้ ตามการตั้งค่าของปลายทาง</span><span class="sxs-lookup"><span data-stu-id="0a631-105">Based on the setting of the destination, a generated document is stored in a previously configured SharePoint folder.</span></span>

<span data-ttu-id="0a631-106">ตั้งค่า **เปิดใช้งาน** เป็น **ใช่** เพื่อใช้การกำหนดค่าคอนฟิก ER เพื่อจัดเตรียมการโอนย้ายข้อมูลจากอินสแตนซ์ Dynamics 365 Finance ของคุณ ไปยังบริการ Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="0a631-106">Set **Enabled** to **Yes** to use your ER configuration to arrange the transfer of data from your Dynamics 365 Finance instance to Microsoft Power BI services.</span></span> <span data-ttu-id="0a631-107">ไฟล์ที่โอนย้ายถูกจัดเก็บในอินสแตนซ์ Microsoft SharePoint Server ที่ต้องถูกตั้งค่าคอนฟิกสำหรับวัตถุประสงค์นั้น</span><span class="sxs-lookup"><span data-stu-id="0a631-107">The transferred files are stored on a Microsoft SharePoint Server instance that must be configured for that purpose.</span></span> <span data-ttu-id="0a631-108">สำหรับข้อมูลเพิ่มเติม ดู [ตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อดึงข้อมูลไปยัง Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="0a631-108">For more information, see [Configure Electronic reporting (ER) to pull data into Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md).</span></span>

<span data-ttu-id="0a631-109">[![หน้าการตั้งค่าปลายทาง](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)</span><span class="sxs-lookup"><span data-stu-id="0a631-109">[![Destination setting page](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a631-110">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0a631-110">Additional resources</span></span>

- [<span data-ttu-id="0a631-111">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="0a631-111">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="0a631-112">ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="0a631-112">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]