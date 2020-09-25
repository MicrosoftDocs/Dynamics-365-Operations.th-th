---
title: ชนิดของปลายทาง ER ใน Power BI
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการกำหนดค่าคอนฟิกชนิดปลายทาง ER ของ Power BI สำหรับเอกสารขาออก
author: NickSelin
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 10.0.09
ms.openlocfilehash: e17ca4eb6b446edd18f4b3c5e697b073f8136a6b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745548"
---
# <a name="power-bi-destination"></a><span data-ttu-id="76d73-103">ปลายทางของ Power BI</span><span class="sxs-lookup"><span data-stu-id="76d73-103">Power BI destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76d73-104">คุณสามารถตั้งค่าคอนฟิกปลายทางของ Microsoft Power BI สำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="76d73-104">You can configure a Microsoft Power BI destination for each folder or file component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="76d73-105">เอกสารที่สร้างขึ้นจะถูกจัดเก็บไว้ในโฟลเดอร์ SharePoint ที่ตั้งค่าคอนฟิกไว้ก่อนหน้านี้ ตามการตั้งค่าของปลายทาง</span><span class="sxs-lookup"><span data-stu-id="76d73-105">Based on the setting of the destination, a generated document is stored in a previously configured SharePoint folder.</span></span>

<span data-ttu-id="76d73-106">ตั้งค่า **เปิดใช้งาน** เป็น **ใช่** เพื่อใช้การตั้งค่าคอนฟิก ER เพื่อจัดเตรียมการโอนย้ายของข้อมูลจากอินสแตนซ์ Dynamics 365 Finance ของคุณ ไปยังบริการ Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="76d73-106">Set **Enabled** to **Yes** to use your ER configuration to arrange the transfer of data from your Dynamics 365 Finance instance to Microsoft Power BI services.</span></span> <span data-ttu-id="76d73-107">ไฟล์ที่โอนย้ายถูกจัดเก็บในอินสแตนซ์ Microsoft SharePoint Server ที่ต้องถูกตั้งค่าคอนฟิกสำหรับวัตถุประสงค์นั้น</span><span class="sxs-lookup"><span data-stu-id="76d73-107">The transferred files are stored on a Microsoft SharePoint Server instance that must be configured for that purpose.</span></span> <span data-ttu-id="76d73-108">สำหรับข้อมูลเพิ่มเติม ดู [ตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อดึงข้อมูลไปยัง Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="76d73-108">For more information, see [Configure Electronic reporting (ER) to pull data into Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md).</span></span>

<span data-ttu-id="76d73-109">[![หน้าการตั้งค่าปลายทาง](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)</span><span class="sxs-lookup"><span data-stu-id="76d73-109">[![Destination setting page](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="76d73-110">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="76d73-110">Additional resources</span></span>

- [<span data-ttu-id="76d73-111">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="76d73-111">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="76d73-112">ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="76d73-112">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
