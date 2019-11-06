---
title: ปิดใช้งานกฎในตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีก
description: หัวข้อนี้อธิบายฟังก์ชันการทำงานของการปิดใช้งานกฎในตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีกใน Microsoft Dynamics 365 Retail
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586308"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="644d1-103">ปิดใช้งานกฎในตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="644d1-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="644d1-104">ผู้ขายปลีกอาจมีสถานการณ์และกระบวนการทางธุรกิจที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="644d1-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="644d1-105">ดังนั้นกฎทั้งหมดที่รวมไว้ตามค่าเริ่มต้นในตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีกจึงไม่สามารถใช้ได้กับผู้ขายปลีกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="644d1-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="644d1-106">เพื่อรองรับความแตกต่าง Microsoft Dynamics 365 Retail จึงมีฟังก์ชันที่สามารถใช้เพื่อปิดใช้งานกฎที่ไม่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="644d1-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="644d1-107">เมื่อต้องการดูรายการของกฎที่มีอยู่ในตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีกในสภาพแวดล้อมของคุณ และเพื่อดูสถานะของกฎแต่ละรายการ ไปที่ **การขายปลีก \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์การขายปลีก** และเลือกแท็บ **การตรวจสอบความถูกต้องของธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="644d1-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="644d1-108">ตามค่าเริ่มต้น สถานะของกฎทั้งหมดตั้งค่าเป็น **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="644d1-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="644d1-109">ดังนั้น จะมีการใช้งานกฎทั้งหมดเพื่อตรวจสอบความถูกต้องของธุรกรรมการขายปลีกก่อนที่จะถูกดึงเข้าไปในใบแจ้งยอดการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="644d1-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="644d1-110">เมื่อต้องการปิดใช้งานกฎ ให้เปลี่ยนสถานะเป็น **ปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="644d1-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="644d1-111">กฎที่ถูกปิดใช้งานจะไม่ได้รับการพิจารณาเมื่อมีการตรวจสอบความถูกต้องของธุรกรรมขายปลีกระหว่างกระบวนการคำนวณของใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="644d1-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="644d1-112">เมื่อต้องการข้ามกระบวนการตรวจสอบความถูกต้องทั้งหมดโดยไม่คำนึงถึงกฎที่เปิดใช้งาน ไปที่ **การขายปลีก \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์การขายปลีก** จากนั้นแท็บ **การตรวจสอบความถูกต้องของธุรกรรม** ตั้งค่าตัวเลือก **ปิดใช้งานตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีก** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="644d1-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="644d1-113">หลังจากที่มีการตั้งค่าตัวเลือกนี้เป็น **ไม่** ตัวเลือกนี้จะไม่สามารถเปลี่ยนกลับเป็น **ใช่** จากอินเทอร์เฟสผู้ใช้ (UI)</span><span class="sxs-lookup"><span data-stu-id="644d1-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
