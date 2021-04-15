---
title: ไคลเอนต์ยกเลิกการเชื่อมต่อ
description: บทความนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าลูกค้าถูกยกเลิกการเชื่อมต่อจากสภาพแวดล้อมของเขาหรือเธอ และไม่รู้ว่าเพราะอะไร
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e9ec43ad0a7d121eb247d81d4b506556a0fa2214
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794912"
---
# <a name="client-disconnects"></a><span data-ttu-id="75505-103">ไคลเอนต์ยกเลิกการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="75505-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="75505-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="75505-104">**Environment details**</span></span> 

<span data-ttu-id="75505-105">ปัญหานี้อาจเกิดขึ้นในสภาพแวดล้อมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="75505-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="75505-106">**อาการ**</span><span class="sxs-lookup"><span data-stu-id="75505-106">**Symptom**</span></span> 

<span data-ttu-id="75505-107">ลูกค้าถูกยกเลิกการเชื่อมต่อจากสภาพแวดล้อมของเขาหรือเธอ และไม่รู้ว่าเพราะอะไร</span><span class="sxs-lookup"><span data-stu-id="75505-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="75505-108">ลูกค้าจะได้รับหนึ่งในข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="75505-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="75505-109">เราได้เสียการเชื่อมต่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="75505-109">We've lost your connection.</span></span> <span data-ttu-id="75505-110">คลิกปิดเพื่อทำงานต่อไป</span><span class="sxs-lookup"><span data-stu-id="75505-110">Click Close to continue working.</span></span>
- <span data-ttu-id="75505-111">การเชื่อมต่อเครือข่ายของคุณอาจขาดหายไป คลิก ลองอีกครั้ง เพื่อลองใหม่</span><span class="sxs-lookup"><span data-stu-id="75505-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="75505-112">**แฟล็กสีแดง**</span><span class="sxs-lookup"><span data-stu-id="75505-112">**Red flag**</span></span>

<span data-ttu-id="75505-113">ปัญหานี้มักเกิดขึ้น เมื่อผู้ใช้อยู่ในระยะการใช้งาน จะเปรียบเทียบข้อมูลระหว่างการผลิต และสภาพแวดล้อมการทดสอบ และลืมว่ามีการย้ายระหว่างเซสชัน</span><span class="sxs-lookup"><span data-stu-id="75505-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="75505-114">ถ้าผู้ใช้ในขั้นตอนนี้ พวกเขามักจะพบปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="75505-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="75505-115">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="75505-115">**Issue**</span></span> 

<span data-ttu-id="75505-116">**ชนิดเบราว์เซอร์:** Google Chrome Internet Explorer และ Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="75505-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="75505-117">Microsoft Dynamics 365 Human Resources ยกเลิกการเชื่อมต่อผู้ใช้ เมื่อเซสชั่นที่แตกต่างกันสองรายการเปิดขึ้นในเวลาเดียวกันสำหรับผู้ใช้เดียวกันและชนิดเบราว์เซอร์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="75505-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="75505-118">(ตัวอย่างเช่น ผู้ใช้ A กำลังดูทั้งสภาพแวดล้อมที่ 1 และ 2 สภาพแวดล้อมใน Chrome) ไม่สำคัญว่าผู้ใช้เปิด windows เบราเซอร์อื่นหรือแท็บอื่น</span><span class="sxs-lookup"><span data-stu-id="75505-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="75505-119">ถ้ามีการใช้ข้อมูลประจำตัวผู้ใช้เดียวกันเพื่อลงชื่อเข้าใช้ในทั้งสภาพแวดล้อมที่ 1 และสภาพแวดล้อมที่ 2 พร้อมกัน และในเบราเซอร์ชนิดเดียวกัน ทรัพยากรบุคคลจะยกเลิกการเชื่อมต่อหนึ่งในเซสชันเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="75505-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="75505-120">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="75505-120">**Solution**</span></span>

<span data-ttu-id="75505-121">ตรวจสอบว่า สภาพแวดล้อมเดียวเท่านั้นถูกเปิดอยู่ในคราวเดียวสำหรับชนิดของเบราเซอร์ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="75505-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="75505-122">ผู้ใช้สามารถเปิดรอบเวลาหลายรอบไปยังสภาพแวดล้อมเดียวกันได้ (นั่นคือ แท็บหลายแท็บในเบราเซอร์เดียวกัน)</span><span class="sxs-lookup"><span data-stu-id="75505-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="75505-123">ผู้ใช้ที่ต้องการข้ามระหว่างสภาพแวดล้อมสองรายการในเวลาเดียวกัน ควรเปิดสภาพแวดล้อมแต่ละรายการในชนิดเบราเซอร์อื่น</span><span class="sxs-lookup"><span data-stu-id="75505-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="75505-124">(ตัวอย่างเช่น ผู้ใช้ A สามารถดูสภาพแวดล้อม 1 ได้ใน Chrome และสภาพแวดล้อม 2 ใน Microsoft Edge)</span><span class="sxs-lookup"><span data-stu-id="75505-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]