<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trace-execution-er-troubleshoot-perf.md" target-language="th-TH">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trace-execution-er-troubleshoot-perf.773b92.aa71db2752889bc905c22bab1cf2fa46d7ee07c7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>aa71db2752889bc905c22bab1cf2fa46d7ee07c7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>67d00b95952faf0db580d341249d4e50be59119c</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\trace-execution-er-troubleshoot-perf.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Trace execution of ER format to troubleshoot performance issues</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การดำเนินการติดตามของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพการทำงาน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to use the performance trace feature in Electronic reporting (ER) to troubleshoot performance issues.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">หัวข้อนี้จะนำเสนอข้อมูลเกี่ยวกับวิธีการใช้คุณลักษณะการติดตามประสิทธิภาพในการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อแก้ไขปัญหาประสิทธิภาพการทำงาน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Trace the execution of ER formats to troubleshoot performance issues</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพการทำงาน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในฐานะที่เป็นส่วนหนึ่งของกระบวนการในการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์ คุณกำหนดวิธีการที่จะใช้ในการดึงข้อมูลออกจาก Microsoft Dynamics 365 for Finance and Operations และป้อนข้อมูลในเอาท์พุทที่สร้างขึ้น</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">คุณลักษณะการติดตามประสิทธิภาพของ ER ช่วยลดเวลาและต้นทุนอย่างมากซึ่งเกี่ยวข้องในการรวบรวมรายละเอียดของการดำเนินการจัดรูปแบบ ER และการใช้เพื่อแก้ไขปัญหาประสิทธิภาพการทำงาน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">บทช่วยสอนนี้จะให้คำแนะนำเกี่ยวกับวิธีการดำเนินการติดตามประสิทธิภาพสำหรับรูปแบบ ER ที่ดำเนินการใน Finance and Operations และวิธีการใช้ข้อมูลจากการติดตามเหล่านี้เพื่อช่วยในการปรับปรุงประสิทธิภาพการทำงาน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ข้อกำหนดเบื้องต้น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To complete the examples in this tutorial, you must have the following access:</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">เพื่อทำตัวอย่างในบทช่วยสอนนี้ให้เสร็จสมบูรณ์ คุณต้องมีการเข้าถึงต่อไปนี้:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Access to Finance and Operations for one of the following roles:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">การเข้าถึง Finance and Operations สำหรับหนึ่งในบทบาทต่อไปนี้:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ผู้ดูแลระบบ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การเข้าถึงอินสแตนซ์ของ Regulatory Configuration Services (RCS) ที่ได้เตรียมใช้งานสำหรับผู้เช่ารายเดียวกันกับ Finance and Operations สำหรับหนึ่งในบทบาทต่อไปนี้:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ผู้ดูแลระบบ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You must also download and locally store the following files.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">นอกจากนี้ คุณต้องดาวน์โหลดและจัดเก็บไฟล์ต่อไปนี้โดยเฉพาะ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>File</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ไฟล์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Content</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ปริมาณความจุ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Performance trace model.version.1</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">แบบจำลองการติดตามประสิทธิภาพการทำงาน รุ่น 1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt>Sample ER data model configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER ตัวอย่าง<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Performance trace metadata.version.1</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">ข้อมูลเมตาการติดตามประสิทธิภาพการทำงาน รุ่น 1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">[</bpt>Sample ER metadata configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>การตั้งค่าคอนฟิกข้อมูลเมตา ER ตัวอย่าง<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Performance trace mapping.version.1.1</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">การแม็ปการติดตามประสิทธิภาพการทำงาน รุ่น 1.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt>Sample ER model mapping configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>การตั้งค่าคอนฟิกการแม็ปแบบจำลองข้อมูล ER ตัวอย่าง<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Performance trace format.version.1.1</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">รูปแบบการติดตามประสิทธิภาพการทำงาน รุ่น 1.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Sample ER format configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>การตั้งค่าคอนฟิกรูปแบบ ER ตัวอย่าง<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Configure ER parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ตั้งค่าคอนฟิกพารามิเตอร์ ER</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การติดตามประสิทธิภาพ ER แต่ละรายการที่สร้างขึ้นใน Finance and Operations จะถูกจัดเก็บเป็นเอกสารแนบของเรกคอร์ดล็อกการดำเนินการ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The Document management (DM) framework of Finance and Operations is used to manage these attachments.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">กรอบงานการจัดการเอกสาร (DM) ของ Finance and Operations ถูกใช้ในการจัดการเอกสารแนบเหล่านี้</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">คุณต้องตั้งค่าคอนฟิกพารามิเตอร์ ER ล่วงหน้า เพื่อระบุชนิดเอกสาร DM ที่ควรใช้เพื่อแนบการติดตามประสิทธิภาพ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In Finance and Operation, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ใน Finance and Operation พื้นที่ทำงาน<bpt id="p1">**</bpt>การรายงานทางอิเล็กทรอนิกส์<ept id="p1">**</ept> ให้เลือก <bpt id="p2">**</bpt>พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">จากนั้น บนหน้า <bpt id="p1">**</bpt>พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์<ept id="p1">**</ept> บนแท็บ <bpt id="p2">**</bpt>เอกสารแนบ<ept id="p2">**</ept> ในฟิลด์ <bpt id="p3">**</bpt>อื่นๆ<ept id="p3">**</ept> ให้เลือกชนิดเอกสาร DM เพื่อใช้สำหรับการติดตามประสิทธิภาพ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">หน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์ใน Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เพื่อให้พร้อมใช้งานในฟิลด์การค้นหา <bpt id="p1">**</bpt>อื่นๆ<ept id="p1">**</ept> ชนิดเอกสาร DM ต้องมีการตั้งค่าคอนฟิกในลักษณะต่อไปนี้บนหน้า <bpt id="p2">**</bpt>ชนิดเอกสาร<ept id="p2">**</ept> (<bpt id="p3">**</bpt>การจัดการองค์กร <ph id="ph1">\&gt;</ph> การจัดการเอกสาร <ph id="ph2">\&gt;</ph> ชนิดเอกสาร<ept id="p3">**</ept>):</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>คลาส:<ept id="p1">**</ept> แนบไฟล์</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>กลุ่ม:<ept id="p1">**</ept> ไฟล์</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Document types page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">หน้าชนิดเอกสารใน Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ชนิดเอกสารที่เลือกต้องพร้อมใช้งานในทุกๆ บริษัทของอินสแตนซ์ Finance and Operations ปัจจุบัน เพราะไฟล์แนบ DM เป็นแบบเฉพาะบริษัท</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Configure RCS parameters</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">ตั้งค่าคอนฟิกพารามิเตอร์ RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การติดตามประสิทธิภาพ ER ซึ่งสร้างขึ้นใน Finance and Operations จะถูกนำเข้าไปยัง RCS สำหรับการวิเคราะห์ โดยใช้ตัวออกแบบรูปแบบ ER และตัวออกแบบการแม็ป ER</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เนื่องจากมีการจัดเก็บการติดตามประสิทธิภาพ ER เป็นเอกสารแนบของเรกคอร์ดบันทึกการดำเนินการที่เกี่ยวข้องกับรูปแบบ ER คุณต้องตั้งค่าคอนฟิกพารามิเตอร์ RCS ล่วงหน้า เพื่อระบุชนิดของเอกสาร DM ที่ควรใช้เพื่อแนบการติดตามประสิทธิภาพ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the instance of RCS that has been provisioned for your company, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในอินสแตนซ์ของ RCS ที่จัดเตรียมให้กับบริษัทของคุณ ในพื้นที่ทำงาน <bpt id="p1">**</bpt>การรายงานทางอิเล็กทรอนิกส์<ept id="p1">**</ept> ให้เลือก <bpt id="p2">**</bpt>พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">จากนั้น บนหน้า <bpt id="p1">**</bpt>พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์<ept id="p1">**</ept> บนแท็บ <bpt id="p2">**</bpt>เอกสารแนบ<ept id="p2">**</ept> ในฟิลด์ <bpt id="p3">**</bpt>อื่นๆ<ept id="p3">**</ept> ให้เลือกชนิดเอกสาร DM เพื่อใช้สำหรับการติดตามประสิทธิภาพ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Electronic reporting parameters page in RCS</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">หน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์ใน RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">เพื่อให้พร้อมใช้งานในฟิลด์การค้นหา <bpt id="p1">**</bpt>อื่นๆ<ept id="p1">**</ept> ชนิดเอกสาร DM ต้องมีการตั้งค่าคอนฟิกในลักษณะต่อไปนี้บนหน้า <bpt id="p2">**</bpt>ชนิดเอกสาร<ept id="p2">**</ept> (<bpt id="p3">**</bpt>การจัดการองค์กร <ph id="ph1">\&gt;</ph> การจัดการเอกสาร <ph id="ph2">\&gt;</ph> ชนิดเอกสาร<ept id="p3">**</ept>):</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>คลาส:<ept id="p1">**</ept> แนบไฟล์</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>กลุ่ม:<ept id="p1">**</ept> ไฟล์</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Design an ER solution</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">ออกแบบโซลูชัน ER</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">สมมติว่าคุณได้เริ่มต้นการออกแบบโซลูชัน ER ใหม่เพื่อสร้างรายงานใหม่ที่แสดงธุรกรรมผู้จัดจำหน่าย</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Currently, you can find the transactions for a selected vendor on the <bpt id="p1">**</bpt>Vendor transactions<ept id="p1">**</ept> page (go to <bpt id="p2">**</bpt>Account payable <ph id="ph1">\&gt;</ph> Vendors <ph id="ph2">\&gt;</ph> All vendors<ept id="p2">**</ept>, select a vendor, and then, on the Action Pane, on the <bpt id="p3">**</bpt>Vendor<ept id="p3">**</ept> tab, in the <bpt id="p4">**</bpt>Transactions<ept id="p4">**</ept> group, select <bpt id="p5">**</bpt>Transactions<ept id="p5">**</ept>).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในปัจจุบัน คุณสามารถค้นหาธุรกรรมสำหรับผู้จัดจำหน่ายที่เลือกบนหน้า <bpt id="p1">**</bpt>ธุรกรรมผู้จัดจำหน่าย<ept id="p1">**</ept> (ไปยัง <bpt id="p2">**</bpt>บัญชีเจ้าหนี้ <ph id="ph1">\&gt;</ph> ผู้จัดจำหน่าย <ph id="ph2">\&gt;</ph> ผู้จัดจำหน่ายทั้งหมด<ept id="p2">**</ept> ให้เลือกผู้จัดจำหน่าย และจากนั้น ในบานหน้าต่างการดำเนินการ บนแท็บ <bpt id="p3">**</bpt>ผู้จัดจำหน่าย<ept id="p3">**</ept> ในกลุ่ม <bpt id="p4">**</bpt>ธุรกรรม<ept id="p4">**</ept> ให้เลือก <bpt id="p5">**</bpt>ธุรกรรม<ept id="p5">**</ept>)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>However, you want to have all vendor transaction at the same time in one electronic document in XML format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">อย่างไรก็ตาม คุณต้องการให้มีธุรกรรมผู้จัดจำหน่ายทั้งหมดในเวลาเดียวกันในเอกสารอิเล็กทรอนิกส์หนึ่งรายการในรูปแบบ XML</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โซลูชันนี้จะประกอบด้วยการตั้งค่าคอนฟิก ER ต่างๆ ที่มีรูปแบบข้อมูลที่จำเป็นต้องใช้ ข้อมูลเมตา การแม็ปแบบจำลอง และส่วนประกอบรูปแบบ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Sign in to the instance of RCS that has been provisioned for your company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ลงชื่อเข้าใช้อินสแตนซ์ของ RCS ที่ได้เตรียมใช้งานสำหรับบริษัทของคุณ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In this tutorial, you will create and modify configurations for the <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept> sample company.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">ในบทช่วยสอนนี้ คุณจะสร้างและปรับเปลี่ยนการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Therefore, make sure that this configuration provider has been added to RCS and selected as active.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ดังนั้น โปรดตรวจสอบให้แน่ใจว่าได้เพิ่มตัวให้บริการการตั้งค่าคอนฟิกนี้ลงใน RCS และได้เลือกเป็นใช้งานอยู่</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For instructions, see the <bpt id="p1">[</bpt>Create configuration providers and mark them as active<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> procedure.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">สำหรับคำแนะนำ ให้ดูที่กระบวนงาน <bpt id="p1">[</bpt>สร้างตัวให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ในพื้นที่ทำงาน <bpt id="p1">**</bpt>การรายงานทางอิเล็กทรอนิกส์<ept id="p1">**</ept> เลือกไทล์ <bpt id="p2">**</bpt>การตั้งค่าคอนฟิกการรายงาน<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในหน้า <bpt id="p1">**</bpt>การตั้งค่าคอนฟิก<ept id="p1">**</ept> นำเข้าการตั้งค่าคอนฟิก ER ที่คุณดาวน์โหลดเป็นข้อกำหนดเบื้องต้นลงใน RCS ตามลำดับต่อไปนี้: รูปแบบข้อมูล ข้อมูลเมตา การแม็ปแบบจำลอง รูปแบบ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For each configuration, follow these steps:</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">สำหรับการตั้งค่าคอนฟิกแต่ละรายการ ทำตามขั้นตอนเหล่านี้:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Exchange <ph id="ph1">\&gt;</ph> Load from XML file<ept id="p1">**</ept>.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">ในบานหน้าต่างการดำเนินการ เลือก <bpt id="p1">**</bpt>แลกเปลี่ยน <ph id="ph1">\&gt;</ph> โหลดจากไฟล์ XML<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the appropriate file for the required ER configuration in XML format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เลือก <bpt id="p1">**</bpt>เรียกดู<ept id="p1">**</ept> เพื่อเลือกไฟล์ที่เหมาะสมสำหรับการตั้งค่าคอนฟิก ER ที่จำเป็นในรูปแบบ XML</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>ตกลง<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Configurations page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">หน้าการตั้งค่าคอนฟิกใน RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Run the ER solution to trace execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">รันโซลูชัน ER เพื่อติดตามการดำเนินการ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Assume that you've finished designing the first version of the ER solution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">สมมติว่าคุณได้ออกแบบโซลูชัน ER รุ่นแรกเสร็จเรียบร้อยแล้ว</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>You now want to test it in your Finance and Operations instance and analyze execution performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ขณะนี้คุณต้องการทดสอบในอินสแตนซ์ Finance and Operations ของคุณ และวิเคราะห์ประสิทธิภาพในการดำเนินงาน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import an ER configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>นำเข้าการตั้งค่าคอนฟิก ER จาก RCS ไปยัง Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Sign in to your Finance and Operations instance.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ลงชื่อเข้าใช้อินสแตนซ์การเงินและการดำเนินงานของคุณ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">สำหรับบทช่วยสอนนี้ คุณจะนำเข้าการตั้งค่าคอนฟิกจากอินสแตนซ์ RCS ของคุณ (ที่ซึ่งคุณออกแบบส่วนประกอบ ER ของคุณ) ลงในอินสแตนซ์ Finance and Operations ของคุณ (ที่ซึ่งคุณทดสอบและใช้งานในที่สุด)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Therefore, you must make sure that all the required artifacts have been prepared.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ดังนั้น คุณต้องตรวจสอบให้แน่ใจว่ามีการจัดเตรียมอาร์ทิแฟกต์ที่จำเป็นทั้งหมดแล้ว</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>For instructions, see the <bpt id="p1">[</bpt>Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept> procedure.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">สำหรับคำแนะนำ โปรดดูกระบวนงาน <bpt id="p1">[</bpt>นำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Follow these steps to import the configurations from RCS into Finance and Operations:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ทำตามขั้นตอนต่อไปนี้เพื่อนำเข้าการตั้งค่าคอนฟิกจาก RCS ไปยัง Finance and Operations:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, on the tile for the <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> configuration provider, select <bpt id="p3">**</bpt>Repositories<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในพื้นที่ทำงาน <bpt id="p1">**</bpt>การรายงานทางอิเล็กทรอนิกส์<ept id="p1">**</ept> บนไทล์สำหรับผู้ให้บริการ การตั้งค่าคอนฟิก <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> เลือก <bpt id="p3">**</bpt>ที่เก็บ<ept id="p3">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>On the <bpt id="p1">**</bpt>Configuration repository<ept id="p1">**</ept> page, select the repository of the <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> type, and then select <bpt id="p3">**</bpt>Open<ept id="p3">**</ept>.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">บนหน้า <bpt id="p1">**</bpt>ที่เก็บการตั้งค่าคอนฟิก<ept id="p1">**</ept> เลือกที่เก็บของชนิด <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> และจากนั้นเลือก <bpt id="p3">**</bpt>เปิด<ept id="p3">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> FastTab, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">บน FastTab <bpt id="p1">**</bpt>การตั้งค่าคอนฟิก<ept id="p1">**</ept> เลือกการตั้งค่าคอนฟิก <bpt id="p2">**</bpt>รูปแบบการติดตามประสิทธิภาพ<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>On the <bpt id="p1">**</bpt>Versions<ept id="p1">**</ept> FastTab, select version <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> of the selected configuration, and then select <bpt id="p3">**</bpt>Import<ept id="p3">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">บน FastTab <bpt id="p1">**</bpt>รุ่น<ept id="p1">**</ept> เลือกรุ่น <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> ของการตั้งค่าคอนฟิกที่เลือก และจากนั้น เลือก <bpt id="p3">**</bpt>นำเข้า<ept id="p3">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Configuration repository page in Finance and Operations</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">หน้าที่เก็บการตั้งค่าคอนฟิกใน Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">รุ่นที่สอดคล้องกันของรูปแบบข้อมูลและการตั้งค่าคอนฟิกการแม็ปแบบจำลอง จะถูกนำเข้าโดยอัตโนมัติเป็นข้อกำหนดเบื้องต้นสำหรับการตั้งค่าคอนฟิกรูปแบบ ER ที่นำเข้า</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Turn on the ER performance trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เปิดการติดตามประสิทธิภาพ ER</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">ใน Finance and Operations ไปที่ <bpt id="p1">**</bpt>การจัดการองค์กร <ph id="ph1">\&gt;</ph> การรายงานทางอิเล็กทรอนิกส์ <ph id="ph2">\&gt;</ph> การตั้งค่าคอนฟิก<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">ในหน้า <bpt id="p1">**</bpt>การตั้งค่าคอนฟิก<ept id="p1">**</ept> บนบานหน้าต่างการดำเนินการ บนแท็บ <bpt id="p2">**</bpt>การตั้งค่าคอนฟิก<ept id="p2">**</ept> ในกลุ่ม <bpt id="p3">**</bpt>การตั้งค่าล่วงหน้า<ept id="p3">**</ept> เลือก <bpt id="p4">**</bpt>พารามิเตอร์ผู้ใช้<ept id="p4">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, follow these steps:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในกล่องโต้ตอบ <bpt id="p1">**</bpt>พารามิเตอร์ผู้ใช้<ept id="p1">**</ept> ในส่วน <bpt id="p2">**</bpt>การติดตามการดำเนินการ<ept id="p2">**</ept> ให้ทำตามขั้นตอนเหล่านี้:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Debug trace format<ept id="p2">**</ept> to start to collect the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในฟิลด์ <bpt id="p1">**</bpt>รูปแบบการติดตามการดำเนินการ<ept id="p1">**</ept> เลือก <bpt id="p2">**</bpt>ดีบักรูปแบบการติดตาม<ept id="p2">**</ept> เมื่อต้องการรวบรวมรายละเอียดของการดำเนินการรูปแบบ ER</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เมื่อมีการเลือกค่านี้ การติดตามประสิทธิภาพจะเก็บรวบรวมข้อมูลเกี่ยวกับเวลาที่ใช้ในการดำเนินการต่อไปนี้:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Running each data source in the model mapping that is called to get data</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การรันแหล่งข้อมูลแต่ละแหล่งในการแม็ปแบบจำลองถูกเรียกเพื่อดึงข้อมูล</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Processing each format item to enter data in the output that is generated</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การประมวลผลรายการรูปแบบแต่ละรายการที่จะป้อนข้อมูลในเอาท์พุทที่ถูกสร้างขึ้น</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You use the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">คุณใช้ฟิลด์ <bpt id="p1">**</bpt>รูปแบบการติดตามการดำเนินการ<ept id="p1">**</ept> เพื่อระบุรูปแบบของการติดตามประสิทธิภาพที่สร้างขึ้น ซึ่งมีการจัดเก็บรายละเอียดการดำเนินการในรูปแบบ ER และองค์ประกอบของการแม็ป</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>By selecting <bpt id="p1">**</bpt>Debug trace format<ept id="p1">**</ept> as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โดยการเลือก <bpt id="p1">**</bpt>ดีบักรูปแบบการติดตาม<ept id="p1">**</ept> คุณจะสามารถวิเคราะห์เนื้อหาของการติดตามในตัวออกแบบการดำเนินงาน ER และดูรูปแบบ ER หรือองค์ประกอบของการแม็ปที่กล่าวถึงในการติดตาม</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Set the following options to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to collect specific details of the execution of the ER model mapping and ER format components:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ตั้งค่าตัวเลือกต่อไปนี้เป็น <bpt id="p1">**</bpt>ใช่<ept id="p1">**</ept> เพื่อรวบรวมรายละเอียดเฉพาะของการดำเนินการของการแม็ปแบบจำลอง ER และส่วนประกอบรูปแบบ ER:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Collect query statistics<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect the following information:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>รวบรวมสถิติการสอบถาม<ept id="p1">**</ept> – เมื่อเปิดตัวเลือกนี้ การติดตามประสิทธิภาพจะรวบรวมข้อมูลต่อไปนี้:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The number of database calls that were made by data sources</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">จำนวนของการเรียกฐานข้อมูลที่ทำโดยแหล่งข้อมูล</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The number of duplicate calls to the database</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">จำนวนครั้งของการเรียกการทำซ้ำไปยังฐานข้อมูล</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Details of the SQL statements that were used to make database calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">รายละเอียดของคำสั่ง SQL ที่ใช้เพื่อทำการเรียกฐานข้อมูล</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Trace access of caching<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>ติดตามการเข้าถึงการแคช<ept id="p1">**</ept> – เมื่อเปิดตัวเลือกนี้ การติดตามประสิทธิภาพจะรวบรวมข้อมูลเกี่ยวกับการใช้แคชของการแม็ปแบบจำลอง ER</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Trace data access<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>ติดตามข้อมูลการเข้าถึง<ept id="p1">**</ept> – เมื่อเปิดตัวเลือกนี้ การติดตามประสิทธิภาพจะรวบรวมข้อมูลเกี่ยวกับจำนวนของการเรียกไปยังฐานข้อมูลสำหรับแหล่งข้อมูลที่ดำเนินการของชนิดรายการเรกคอร์ด</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Trace list enumeration<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>การแจงนับรายการติดตาม<ept id="p1">**</ept> – เมื่อเปิดตัวเลือกนี้ การติดตามประสิทธิภาพจะรวบรวมข้อมูลเกี่ยวกับจำนวนของเรกคอร์ดที่ถูกร้องขอจากแหล่งข้อมูลของชนิดรายการเรกคอร์ด</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The parameters in the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box are specific to the user and the current company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">พารามิเตอร์ในกล่องโต้ตอบ <bpt id="p1">**</bpt>พารามิเตอร์ของผู้ใช้<ept id="p1">**</ept> ที่เฉพาะเจาะจงสำหรับผู้ใช้และบริษัทปัจจุบัน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>User parameters dialog box in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">กล่องโต้ตอบพารามิเตอร์ของผู้ใช้ใน Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Run the ER format</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>รันรูปแบบ ER</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In Finance and Operations, select the <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> company.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">ใน Finance and Operations เลือกบริษัท <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">ไปที่ <bpt id="p1">**</bpt>การจัดการองค์กร <ph id="ph1">\&gt;</ph> การรายงานทางอิเล็กทรอนิกส์ <ph id="ph2">\&gt;</ph> การตั้งค่าคอนฟิก<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> item.</source><target logoport:matchpercent="77" state="translated" state-qualifier="leveraged-mt">บนหน้า <bpt id="p1">**</bpt>การตั้งค่าคอนฟิก<ept id="p1">**</ept> ในแผนภูมิการตั้งค่าคอนฟิก เลือกรายการ <bpt id="p2">**</bpt>รูปแบบการติดตามประสิทธิภาพ<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Run<ept id="p1">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">บนบานหน้าต่างการดำเนินการ เลือก <bpt id="p1">**</bpt>รัน<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Notice that the file that is generated presents information about 265 transactions for six vendors.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โปรดสังเกตว่าไฟล์ที่สร้างขึ้นแสดงข้อมูลเกี่ยวกับธุรกรรม 265 รายการสำหรับผู้จัดจำหน่ายหกราย</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Review the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ตรวจทานการติดตามการดำเนินการ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>ส่งออกการติดตามที่สร้างขึ้นจาก Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การติดตามประสิทธิภาพถูกแยกจากรูปแบบ ER ต้นทาง และสามารถทำให้เป็นแบบอนุกรมกับไฟล์ zip ภายนอก</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configuration debug logs<ept id="p1">**</ept>.</source><target logoport:matchpercent="88" state="translated" state-qualifier="fuzzy-match">ใน Finance and Operations ไปที่ <bpt id="p1">**</bpt>การจัดการองค์กร <ph id="ph1">\&gt;</ph> การรายงานทางอิเล็กทรอนิกส์ <ph id="ph2">\&gt;</ph> บันทึกดีบักของการตั้งค่าคอนฟิก<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Electronic reporting run logs<ept id="p1">**</ept> page, in the left pane, in the <bpt id="p2">**</bpt>Configuration name<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> to find the log records that have been generated by the execution of the <bpt id="p4">**</bpt>Performance trace format<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">บนหน้า <bpt id="p1">**</bpt>บันทึกการรันการรายงานทางอิเล็กทรอนิกส์<ept id="p1">**</ept> ในบานหน้าต่างด้านซ้าย ในฟิลด์ <bpt id="p2">**</bpt>ชื่อการตั้งค่าคอนฟิก<ept id="p2">**</ept> เลือก <bpt id="p3">**</bpt>รูปแบบการติดตามประสิทธิภาพ<ept id="p3">**</ept> เพื่อค้นหาเรกคอร์ดล็อกที่สร้างขึ้นโดยการดำเนินการของการตั้งค่าคอนฟิก <bpt id="p4">**</bpt>รูปแบบการติดตามประสิทธิภาพ<ept id="p4">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Select the <bpt id="p1">**</bpt>Attachments<ept id="p1">**</ept> button (the paper clip symbol) in the upper-right corner of the page, or press <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">เลือกปุ่ม <bpt id="p1">**</bpt>เอกสารแนบ<ept id="p1">**</ept> (สัญลักษณ์คลิปหนีบกระดาษ) ในมุมขวาบนของหน้า หรือกด <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Attachments button on the Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">ปุ่มเอกสารแนบในหน้าบันทึกการรันการรายงานทางอิเล็กทรอนิกส์ใน Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>On the <bpt id="p1">**</bpt>Attachments for Electronic reporting run logs<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Open<ept id="p2">**</ept> to get the performance trace as a zip file and store it locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">บนหน้า <bpt id="p1">**</bpt>เอกสารแนบสำหรับบันทึกการรันการรายงานทางอิเล็กทรอนิกส์<ept id="p1">**</ept> ในบานหน้าต่างการดำเนินการ ให้เลือก <bpt id="p2">**</bpt>เปิด<ept id="p2">**</ept> เพื่อรับการติดตามประสิทธิภาพเป็นไฟล์ zip และจัดเก็บไว้ภายใน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Attachments for Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เอกสารแนบสำหรับหน้าบันทึกการรันการรายงานทางอิเล็กทรอนิกส์ใน Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The trace that is generated has a reference to the source ER report via a unique report identifier in <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> format only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การติดตามที่สร้างขึ้นมีการอ้างอิงไปยังรายงาน ER ของแหล่งข้อมูลผ่านตัวระบุรายงานที่ไม่ซ้ำกันในรูปแบบ <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> เท่านั้น</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The version numbering of the format isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การกำหนดหมายเลขรุ่นของรูปแบบไม่ได้รับการพิจารณา</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โปรดสังเกตว่าความสัมพันธ์ระหว่างการติดตามประสิทธิภาพที่ถูกสร้างขึ้นสำหรับรูปแบบ ER ที่ดำเนินการ และการแม็ปแบบจำลอง ER จะขึ้นอยู่กับตัวอธิบายรากที่ใช้และแบบจำลองข้อมูลทั่วไป</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The version numbering of the format and model mapping isn't considered.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">การกำหนดหมายเลขรุ่นของรูปแบบและการแม็ปแบบจำลองไม่ได้รับการพิจารณา</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The setting of the <bpt id="p1">**</bpt>Default for model mapping<ept id="p1">**</ept> flag for the model mapping also isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">นอกจากนี้ จะไม่มีการพิจารณาการตั้งค่าของแฟล็ก <bpt id="p1">**</bpt>ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง<ept id="p1">**</ept> สำหรับการแม็ปแบบจำลอง</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import the generated trace into RCS</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>นำเข้าการติดตามที่สร้างลงใน RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In RCS, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">ใน RCS พื้นที่ทำงาน <bpt id="p1">**</bpt>การรายงานทางอิเล็กทรอนิกส์<ept id="p1">**</ept> เลือกไทล์ <bpt id="p2">**</bpt>การตั้งค่าคอนฟิกการรายงาน<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, expand the <bpt id="p2">**</bpt>Performance trace model<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในหน้า <bpt id="p1">**</bpt>การตั้งค่าคอนฟิก<ept id="p1">**</ept> ในแผนภูมิการตั้งค่าคอนฟิก ให้ขยายรายการ <bpt id="p2">**</bpt>แบบจำลองการติดตามประสิทธิภาพ<ept id="p2">**</ept> และเลือกรายการ <bpt id="p3">**</bpt>รูปแบบการติดตามประสิทธิภาพ<ept id="p3">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">บนบานหน้าต่างการดำเนินการ เลือก <bpt id="p1">**</bpt>ตัวออกแบบ<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">บนหน้า <bpt id="p1">**</bpt>ตัวออกแบบรูปแบบ<ept id="p1">**</ept> บนบานหน้าต่างการดำเนินการ ให้เลือก <bpt id="p2">**</bpt>การติดตามประสิทธิภาพ<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In the <bpt id="p1">**</bpt>Performance trace result settings<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>Import performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในกล่องโต้ตอบ <bpt id="p1">**</bpt>การตั้งค่าผลการติดตามประสิทธิภาพ<ept id="p1">**</ept> ให้เลือก <bpt id="p2">**</bpt>นำเข้าการติดตามประสิทธิภาพ<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the zip file that you exported from Finance and Operations earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เลือก <bpt id="p1">**</bpt>เรียกดู<ept id="p1">**</ept> เพื่อเลือกไฟล์ zip ที่คุณส่งออกจาก Finance and Operations ก่อนหน้านี้</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>ตกลง<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Performance trace result settings dialog box in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">กล่องโต้ตอบการตั้งค่าผลการติดตามประสิทธิภาพใน RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use the performance trace for analysis in RCS – Format execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ใช้การติดตามประสิทธิภาพสำหรับการวิเคราะห์ใน RCS – การดำเนินการรูปแบบ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In RCS, on the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Expand/collapse<ept id="p2">**</ept> to expand the content of all format items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ใน RCS บนหน้า <bpt id="p1">**</bpt>ตัวออกแบบรูปแบบ<ept id="p1">**</ept> ให้เลือก <bpt id="p2">**</bpt>ขยาย/ยุบ<ept id="p2">**</ept> เพื่อขยายเนื้อหาของรายการรูปแบบทั้งหมด</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Notice that additional information is shown for some items of the current format:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โปรดสังเกตว่ามีการแสดงข้อมูลเพิ่มเติมสำหรับบางรายการของรูปแบบปัจจุบัน:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The actual time that was spent entering data in the generated output by using the format item</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เวลาจริงที่ใช้ในการป้อนข้อมูลในเอาท์พุทที่สร้างขึ้นโดยใช้รายการรูปแบบ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The same time expressed as a percentage of the total time that was spent generating the whole output</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เวลาเดียวกันที่แสดงเป็นเปอร์เซ็นต์ของเวลาทั้งหมดที่ใช้ในการสร้างเอาท์พุททั้งหมด</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Format designer page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">หน้าตัวออกแบบรูปแบบใน RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Close <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">ปิดหน้า <bpt id="p1">**</bpt>ตัวออกแบบรูปแบบ<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>ใช้การติดตามประสิทธิภาพสำหรับการวิเคราะห์ใน RCS – การแม็ปรูปแบบ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ใน RCS บนหน้า <bpt id="p1">**</bpt>การตั้งค่าคอนฟิก<ept id="p1">**</ept> ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือกรายการ <bpt id="p2">**</bpt>การแม็ปการติดตามประสิทธิภาพ<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="85" state="translated" state-qualifier="leveraged-inherited">บนบานหน้าต่างการดำเนินการ เลือก <bpt id="p1">**</bpt>ตัวออกแบบ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>ตัวออกแบบ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>On the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">บนหน้า <bpt id="p1">**</bpt>ตัวออกแบบการแม็ปแบบจำลอง<ept id="p1">**</ept> บนบานหน้าต่างการดำเนินการ ให้เลือก <bpt id="p2">**</bpt>การติดตามประสิทธิภาพ<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Select the trace that you imported earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เลือกการติดตามที่คุณนำเข้าก่อนหน้านี้</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>ตกลง<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Notice that new information becomes available for some data source items of the current model mapping:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โปรดสังเกตว่าข้อมูลใหม่จะกลายเป็นพร้อมใช้งานสำหรับรายการแหล่งข้อมูลบางอย่างของการแม็ปแบบจำลองปัจจุบัน:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The actual time that was spent getting data by using the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เวลาจริงที่ใช้ในการเรียกข้อมูลโดยใช้แหล่งข้อมูล</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The same time expressed as a percentage of the total time that was spent running the whole model mapping</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">เวลาเดียวกันที่แสดงเป็นเปอร์เซ็นต์ของเวลาทั้งหมดที่ใช้ในการรันการแม็ปแบบจำลองทั้งหมด</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source is run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โปรดสังเกตว่า ER แจ้งให้คุณทราบว่าการแม็ปแบบจำลองปัจจุบันจะทำซ้ำคำขอฐานข้อมูล ในขณะที่แหล่งข้อมูล VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum ถูกรัน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การทำซ้ำนี้เกิดขึ้นเนื่องจากรายการของธุรกรรมผู้จัดจำหน่ายถูกเรียกสองครั้งสำหรับเรกคอร์ดผู้จัดจำหน่ายที่ทำซ้ำแต่ละรายการ:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>One call is made to enter details of each transaction in the data model, based on configured bindings.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">มีการเรียกหนึ่งครั้งเพื่อป้อนรายละเอียดของแต่ละธุรกรรมในแบบจำลองข้อมูล ซึ่งขึ้นกับการผูกข้อมูลที่ตั้งค่าคอนฟิก</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>One call is made to enter the calculated number of transactions per vendor in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">มีการทำการเรียกหนึ่งครั้งเพื่อป้อนจำนวนของธุรกรรมที่คำนวณได้สำหรับผู้จัดจำหน่ายแต่ละรายในแบบจำลองข้อมูล</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Message about duplicate database requests on the Model mapping designer page in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ข้อความเกี่ยวกับการร้องขอฐานข้อมูลที่ซ้ำกันบนหน้าตัวออกแบบการแม็ปแบบจำลองใน RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ค่า <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> บ่งชี้ว่าตาราง VendTrans ถูกเรียก 530 ครั้งเพื่อส่งคืนเรกคอร์ดจากตารางนั้นไปยังแหล่งข้อมูล VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ค่า <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept>บ่งชี้ว่ามีการเรียกแหล่งข้อมูล VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum ถูกเรียก 530 ครั้ง เพื่อส่งคืนเรกคอร์ดจากแหล่งข้อมูลนั้นและป้อนรายละเอียดจากรายการนั้นในแบบจำลองข้อมูล</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>We recommend that you use caching for the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เราขอแนะนำให้คุณใช้การแคชสำหรับแหล่งข้อมูล VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum เพื่อลดจำนวนของการเรียกที่ถูกทำเพื่อดูรายละเอียดสำหรับธุรกรรม 265 รายการ และช่วยปรับปรุงประสิทธิภาพการทำงานของการแม็ปแบบจำลอง</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">นอกจากนี้ ยังอาจเป็นประโยชน์ในการลดจำนวนการเรียกที่ทำไปยังแหล่งข้อมูล LedgerTransTypeList</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>This data source is used to associate each value of the <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> enumeration with its label.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">แหล่งข้อมูลนี้ใช้ในการเชื่อมโยงค่าแต่ละค่าของการแจงนับ <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> กับป้ายชื่อ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โดยใช้แหล่งข้อมูลนี้ คุณสามารถค้นหาป้ายชื่อที่เหมาะสม และป้อนในรูปแบบข้อมูลสำหรับธุรกรรมผู้จัดจำหน่ายแต่ละราย</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The current number of calls to this data source (9,027) is quite high for 265 transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">จำนวนครั้งปัจจุบันของการเรียกไปยังแหล่งข้อมูลนี้ (9,027) ค่อนข้างสูงสำหรับธุรกรรม 265 รายการ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Model mapping designer page in RCS, showing 9,027 calls to the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">หน้าตัวออกแบบการแม็ปแบบจำลองใน RCS ซึ่งแสดงการเรียก 9,027 รายการไปยังแหล่งข้อมูล</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Improve the model mapping based on information from the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ปรับปรุงการแม็ปแบบจำลองตามข้อมูลจากการติดตามการดำเนินการ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Modify the logic of the model mapping</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">ปรับเปลี่ยนตรรกะของการแม็ปแบบจำลอง</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Follow these steps to use caching, to help prevent duplicate calls to the database:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ทำตามขั้นตอนต่อไปนี้เพื่อใช้การแม็ปการติดตามประสิทธิภาพ เพื่อช่วยป้องกันการเรียกซ้ำไปยังฐานข้อมูล:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>In RCS, on the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> pane, select the <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ใน RCS บนหน้า <bpt id="p1">**</bpt>ตัวออกแบบการแม็ปแบบจำลอง<ept id="p1">**</ept> ในบานหน้าต่าง <bpt id="p2">**</bpt>แหล่งข้อมูล<ept id="p2">**</ept> ให้เลือกรายการ <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เลือก <bpt id="p1">**</bpt>แคช<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Expand the <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> item, expand the list of one-to-many relations for the VendTable data source (the <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p2">**</ept> item), and select the <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ขยายรายการ <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> ขยายรายการของความสัมพันธ์แบบหนึ่งต่อกลุ่มสำหรับแหล่งข้อมูล VendTable (รายการ <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>ความสัมพันธ์<ept id="p2">**</ept>) และเลือกรายการ <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">เลือก <bpt id="p1">**</bpt>แคช<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Caching setup to help prevent duplicate calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การแคชการตั้งค่าเพื่อช่วยป้องกันการเรียกซ้ำ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ทำตามขั้นตอนต่อไปนี้เพื่อนำแหล่งข้อมูล LedgerTransTypeList เข้าไปในขอบเขตของแหล่งข้อมูล VendTable:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>In the <bpt id="p1">**</bpt>Data source types<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Calculated field<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในบานหน้าต่าง <bpt id="p1">**</bpt>ชนิดแหล่งข้อมูล<ept id="p1">**</ept> ให้ขยายรายการ <bpt id="p2">**</bpt>ฟังก์ชัน<ept id="p2">**</ept> และเลือกรายการ <bpt id="p3">**</bpt>ฟิลด์ที่คำนวณได้<ept id="p3">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, select the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในบานหน้าต่าง <bpt id="p1">**</bpt>แหล่งข้อมูล<ept id="p1">**</ept> ให้เลือกรายการ <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>เพิ่ม<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">ในฟิลด์ <bpt id="p1">**</bpt>ชื่อ<ept id="p1">**</ept> ให้ป้อน <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">เลือก <bpt id="p1">**</bpt>แก้ไขสูตร<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">ในฟิลด์ <bpt id="p1">**</bpt>สูตร<ept id="p1">**</ept> ให้ป้อน <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>บันทึก<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ปิดหน้า <bpt id="p1">**</bpt>ตัวแก้ไขสูตร<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>ตกลง<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Follow these steps to do caching of the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ทำตามขั้นตอนต่อไปนี้เพื่อทำการแคชของฟิลด์ <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept>:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Select the <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept> item.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">เลือกรายการ <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">เลือก <bpt id="p1">**</bpt>แคช<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Select the <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เลือกรายการ <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">เลือก <bpt id="p1">**</bpt>แคช<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Caching setup for the $TransType field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">การแคชการตั้งค่าสำหรับฟิลด์ $TransType</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Follow these steps to change the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> field so that it starts to use the cached <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ทำตามขั้นตอนเหล่านี้เพื่อเปลี่ยนแปลงฟิลด์ <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> เพื่อให้เริ่มต้นการใช้ฟิลด์ <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> ที่แคช:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item, expand the <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p3">**</ept> item, expand the <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> item, and select the <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในบานหน้าต่าง <bpt id="p1">**</bpt>แหล่งข้อมูล<ept id="p1">**</ept> ให้ขยายรายการ <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> ขยายรายการ <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>ความสัมพันธ์<ept id="p3">**</ept> ขยายรายการ <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> และเลือกรายการ <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Select <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>แก้ไข<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">เลือก <bpt id="p1">**</bpt>แก้ไขสูตร<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, find the following expression:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในฟิลด์ <bpt id="p1">**</bpt>สูตร<ept id="p1">**</ept> ให้ค้นหานิพจน์ต่อไปนี้:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter the following expression:</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">ในฟิลด์ <bpt id="p1">**</bpt>สูตร<ept id="p1">**</ept> ให้ป้อนนิพจน์ต่อไปนี้:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType))</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>บันทึก<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">ปิดหน้า <bpt id="p1">**</bpt>ตัวแก้ไขสูตร<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>ตกลง<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>บันทึก<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Close the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">ปิดหน้า <bpt id="p1">**</bpt>ตัวออกแบบการแม็ปแบบจำลอง<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Close the <bpt id="p1">**</bpt>Model mappings<ept id="p1">**</ept> page.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">ปิดหน้า <bpt id="p1">**</bpt>การแม็ปแบบจำลอง<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Complete the modified version of the ER model mapping</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ดำเนินการรุ่นที่แก้ไขของการแม็ปแบบจำลอง ER ให้เสร็จสมบูรณ์</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Versions<ept id="p2">**</ept> FastTab, select version <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> of the <bpt id="p4">**</bpt>Performance trace mapping<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ใน RCS บนหน้า <bpt id="p1">**</bpt>การตั้งค่าคอนฟิก<ept id="p1">**</ept> บน FastTab <bpt id="p2">**</bpt>รุ่น<ept id="p2">**</ept> ให้เลือกรุ่น <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> ของการตั้งค่าคอนฟิก <bpt id="p4">**</bpt>การแม็ปการติดตามประสิทธิภาพ<ept id="p4">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select <bpt id="p1">**</bpt>Change status<ept id="p1">**</ept>.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">เลือก <bpt id="p1">**</bpt>เปลี่ยนแปลงสถานะ<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Select <bpt id="p1">**</bpt>Complete<ept id="p1">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">เลือก <bpt id="p1">**</bpt>เสร็จสมบูรณ์<ept id="p1">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Import the modified ER model mapping configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">นำเข้าการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ที่แก้ไขจาก RCS ไปยัง Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import an ER configuration from RCS into Finance and Operations<ept id="p1">](#import-configuration)</ept> section earlier in this topic to import version 1.2 of the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> configuration into Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ทำซ้ำขั้นตอนในส่วน <bpt id="p1">[</bpt>นำเข้าการตั้งค่าคอนฟิก ER จาก RCS ไปยัง Finance and Operations<ept id="p1">](#import-configuration)</ept> ก่อนหน้านี้ในหัวข้อนี้ เพื่อนำเข้ารุ่น 1.2 ของการตั้งค่าคอนฟิก <bpt id="p2">**</bpt>การแม็ปการติดตามประสิทธิภาพ<ept id="p2">**</ept> ไปยัง Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Run the modified ER solution to trace execution</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">รันโซลูชัน ER ที่แก้ไขเพื่อติดตามการดำเนินการ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Run the ER format</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">รันรูปแบบ ER</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ทำซ้ำขั้นตอนในส่วน <bpt id="p1">[</bpt>รันรูปแบบ ER<ept id="p1">](#run-format)</ept> ก่อนหน้าในหัวข้อนี้ เพื่อสร้างการติดตามประสิทธิภาพใหม่</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Review the execution trace</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">ตรวจทานการติดตามการดำเนินการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-mt">ส่งออกการติดตามที่สร้างขึ้นจาก Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Export the generated trace from Finance and Operations<ept id="p1">](#export-trace)</ept> section earlier in this topic to save a new performance trace locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ทำซ้ำขั้นตอนในส่วน <bpt id="p1">[</bpt>ส่งออกการติดตามที่สร้างขึ้นจาก Finance and Operations<ept id="p1">](#export-trace)</ept> ก่อนหน้านี้ในหัวข้อนี้ เพื่อบันทึกการติดตามประสิทธิภาพใหม่ภายในเครื่อง</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Import the generated trace into RCS</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">นำเข้าการติดตามที่สร้างลงใน RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import the generated trace into RCS<ept id="p1">](#import-trace)</ept> section earlier in this topic to import the new performance trace into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ทำซ้ำขั้นตอนในส่วน <bpt id="p1">[</bpt>นำเข้าการติดตามที่สร้างขึ้นใน RCS<ept id="p1">](#import-trace)</ept> ก่อนหน้าในหัวข้อนี้ เพื่อนำเข้าการติดตามประสิทธิภาพใหม่ไปยัง RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">ใช้การติดตามประสิทธิภาพสำหรับการวิเคราะห์ใน RCS – การแม็ปรูปแบบ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Use the performance trace for analysis in RCS – Model mapping<ept id="p1">](#use-trace)</ept> section earlier in this topic to analyze the latest performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ทำซ้ำขั้นตอนในส่วน <bpt id="p1">[</bpt>ใช้การติดตามประสิทธิภาพสำหรับการวิเคราะห์ใน RCS – การแม็ปแบบจำลอง<ept id="p1">](#use-trace)</ept> ก่อนหน้านี้ในหัวข้อนี้ เพื่อวิเคราะห์การติดตามประสิทธิภาพล่าสุด</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โปรดสังเกตว่าการปรับปรุงที่คุณทำไปยังการแม็ปแบบจำลอง มีการตัดการสอบถามที่ซ้ำกันไปยังฐานข้อมูล</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>The number of calls to database tables and data sources for this model mapping has been also reduced.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">นอกจากนี้ ยังมีการลดจำนวนของการเรียกไปยังตารางฐานข้อมูลและแหล่งข้อมูลสำหรับการแม็ปแบบจำลองนี้ด้วย</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Therefore, the performance of the whole ER solution has improved.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ดังนั้น ประสิทธิภาพการทำงานของโซลูชัน ER ทั้งหมดได้รับการปรับปรุง</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Trace information for the VendTable data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">ข้อมูลการติดตามสำหรับแหล่งข้อมูล VendTable ในหน้าตัวออกแบบการแม็ปแบบจำลองใน RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>In the trace information, the value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> for the VendTable data source indicates that this data source was called 12 times.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในข้อมูลการติดตาม ค่า <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> สำหรับแหล่งข้อมูล VendTable บ่งชี้ว่าแหล่งข้อมูลนี้ถูกเรียก 12 ครั้ง</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that six calls were translated to database calls to the VendTable table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ค่า <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> บ่งชี้ว่ามีการแปลการเรียก 6 ครั้งเป็นการเรียกฐานข้อมูลไปยังตาราง VendTable</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ค่า <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> บ่งชี้ว่าเรกคอร์ดที่นำมาใช้จากฐานข้อมูลถูกแคช และมีการประมวลผลการเรียกอีกหกครั้งโดยใช้แคช</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โปรดสังเกตว่ามีการลดจำนวนการเรียกไปยังแหล่งข้อมูล LedgerTransTypeList จาก 9,027 เป็น 240</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Trace information for the LedgerTransTypeList data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">ข้อมูลการติดตามสำหรับแหล่งข้อมูล LedgerTransTypeList ในหน้าตัวออกแบบการแม็ปแบบจำลองใน RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Review the execution trace in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ตรวจทานการติดตามการดำเนินการใน Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">นอกจาก RCS รุ่นบางรุ่นของ Finance and Operations อาจมีความสามารถสำหรับประสบการณ์นักออกแบบกรอบงาน ER</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>These versions of Finance and Operations have an <bpt id="p1">**</bpt>Enable design mode<ept id="p1">**</ept> option that can be turned on.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">รุ่นของ Finance and Operations มีตัวเลือก <bpt id="p1">**</bpt>เปิดใช้งานโหมดการออกแบบ<ept id="p1">**</ept> ที่สามารถเปิดได้</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>You can find this option on the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept> page, which you can open from the <bpt id="p3">**</bpt>Electronic reporting<ept id="p3">**</ept> workspace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">คุณสามารถค้นหาตัวเลือกนี้บนแท็บ <bpt id="p1">**</bpt>ทั่วไป<ept id="p1">**</ept> ของหน้า <bpt id="p2">**</bpt>พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์<ept id="p2">**</ept> ซึ่งคุณสามารถเปิดได้จากพื้นที่ทำงาน <bpt id="p3">**</bpt>การรายงานทางอิเล็กทรอนิกส์<ept id="p3">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Enable design mode option on the Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เปิดใช้งานตัวเลือกโหมดการออกแบบในหน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์ใน Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ถ้าคุณใช้ Finance and Operations รุ่นใดรุ่นหนึ่งต่อไปนี้ คุณสามารถวิเคราะห์รายละเอียดของการติดตามประสิทธิภาพที่สร้างขึ้นโดยตรงใน Finance and Operations</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>You don't have to export them from Finance and Operation and import them into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">คุณไม่จำเป็นต้องส่งออกจาก Finance and Operations และนำเข้าไปยัง RCS</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Review the execution trace by using external tools</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ตรวจทานการติดตามการดำเนินการโดยใช้เครื่องมือภายนอก</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Configure user parameters</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">ตั้งค่าคอนฟิกพารามิเตอร์ผู้ใช้</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="75" state="translated" state-qualifier="leveraged-inherited">ใน Finance and Operations ไปที่ <bpt id="p1">**</bpt>การจัดการองค์กร <ph id="ph1">\&gt;</ph> การรายงานทางอิเล็กทรอนิกส์ <ph id="ph2">\&gt;</ph> การตั้งค่าคอนฟิก<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="72" state="translated" state-qualifier="leveraged-inherited">ในหน้า <bpt id="p1">**</bpt>การตั้งค่าคอนฟิก<ept id="p1">**</ept> บนบานหน้าต่างการดำเนินการ บนแท็บ <bpt id="p2">**</bpt>การตั้งค่าคอนฟิก<ept id="p2">**</ept> ในกลุ่ม <bpt id="p3">**</bpt>การตั้งค่าล่วงหน้า<ept id="p3">**</ept> เลือก <bpt id="p4">**</bpt>พารามิเตอร์ผู้ใช้<ept id="p4">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, in the <bpt id="p3">**</bpt>Execution trace format<ept id="p3">**</ept> field, select <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ในกล่องโต้ตอบ <bpt id="p1">**</bpt>พารามิเตอร์ผู้ใช้<ept id="p1">**</ept> ในส่วน <bpt id="p2">**</bpt>การติดตามการดำเนินการ<ept id="p2">**</ept> ในฟิลด์ <bpt id="p3">**</bpt>รูปแบบการติดตามการดำเนินการ<ept id="p3">**</ept> เลือก <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Run the ER format</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">รันรูปแบบ ER</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">ทำซ้ำขั้นตอนในส่วน <bpt id="p1">[</bpt>รันรูปแบบ ER<ept id="p1">](#run-format)</ept> ก่อนหน้าในหัวข้อนี้ เพื่อสร้างการติดตามประสิทธิภาพใหม่</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Notice that the web browser offers a zip file for download.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">โปรดสังเกตว่าเว็บเบราเซอร์มีไฟล์ซิปสำหรับการดาวน์โหลด</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>This file contains the performance trace in PerfView format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ไฟล์นี้มีการติดตามประสิทธิภาพในรูปแบบ PerfView</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">จากนั้น คุณสามารถใช้เครื่องมือวิเคราะห์ประสิทธิภาพ PerfView เพื่อวิเคราะห์รายละเอียดของการดำเนินการของรูปแบบ ER</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>