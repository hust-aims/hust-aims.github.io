---
layout: default
title: "Home"
toc: true
url: /
---
#### **Welcome to AIMS Group!**
AIMS group belongs to [Data Storage and Application Lab](http://storage.hust.edu.cn/). AIMS refers to Advanced Intelligent Memory Systems. We aim at building high performance and energy-efficient systems with emerging devices and technologies (e.g., non-volatile memories, key-value storage, solid-state drive, high performance compression, cloud object store, and emerging NVMs).

The research group has long been dedicated to cutting-edge research on advanced intelligent storage systems, with a focus on high-performance and energy-efficient storage solutions based on emerging memory technologies and innovative architectures. The group’s primary research areas include:

1. **Full-stack Processing-in-Memory (PiM) Technologies**: Covering the entire stack from device characteristics and chip architectures to system-level optimizations, with an emphasis on breakthroughs in PiM chip design, dedicated compiler toolchains, and compensation for non-idealities.

2. **Advanced Memory Systems**: Investigating high-performance architectures for emerging non-volatile memory (NVM), security-enhancing mechanisms, and technologies for large-capacity storage.

3. **Intelligent Storage Devices**: Exploring co-optimization of hardware architectures and system software for computational storage devices.

Our group has published several papers on international conferences like ISCA, MICRO, DAC, DATE, ICCAD, ICPP, MSST, ICCD, LCTES, etc. as well as some top journals including IEEE TC, IEEE TCAD, IEEE T-ED, ACM TACO, ACM TODAES, JSA, etc.


<head>
    <meta charset="utf-8">
    <title>picplay</title>
    <style>
        #divout {
            max-width: 600px;
            max-height: 400px;
            position: relative;
            margin: 0 auto;
        }

        .imgdiv img {
            width: 100%;
        }
    
        .imgdiv {
            display: none;
        }
    
        .dotdiv {
            text-align: center;
            position: absolute;
            width: 100%;
            bottom: -30px;
        }
    
        .dot {
            width: 16px;
            height: 16px;
            display: inline-block;
            background: #bbbbbb;
            border-radius: 10px;
            margin: 0 12px;
        }
    
        .title {
            font-size: 18px;
            color: #0099FF;
            position: absolute;
            text-align: center;
            font-weight: 700;
            width: 100%;
            bottom: 10px;
        }
    
        .active {
            background-color: #717171;
        }
    
        #arrow {
            position: absolute;
            top: 50%;
            margin-top: -30px;
            width: 100%;
            opacity: .3;
            transition: opacity 2s;
        }
    
        #divout:hover #arrow {
            opacity: .9;
        }
    
        #arrow img {
            cursor: pointer;
        }
    
        .imgdiv {
            animation: fade 1.5s;
        }
    
        @keyframes fade {
            from {
                opacity: .3;
            }
    
            to {
                opacity: 1;
            }
        }
    </style>
</head>

<body>
    <!--    div#divout>(div.imgdiv>img+div.title{标题文本$})*4 +(div.dotdiv>span.dot*4)-->
    <div id="divout">
        <div class="imgdiv" style="display: block">
            <img src="/assets/img/league_building/2021_autum/2021_11_autumn_43.png" height="80%" width="80%" alt="">
            <div class="title">Group Party 2021</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/league_building/2020_group_party.jpg" height="80%" width="80%" alt="">
            <div class="title">Group Party 2020</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/award.png" height="80%" width="80%" alt="">
            <div class="title">OlympusMons Award</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/ICCD17.jpg" height="80%" width="80%" alt="">
            <div class="title">ICCD 2017</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/ICCD19.jpg" height="80%" width="80%" alt="">
            <div class="title">ICCD 2019</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/DATE19.jpg" height="80%" width="80%" alt="">
            <div class="title">DATE 2019</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/DATE23.jpg" height="80%" width="80%" alt="">
            <div class="title">DATE 2023</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/DATE24.jpg" height="80%" width="80%" alt="">
            <div class="title">DATE 2024</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/DAC24.jpg" height="80%" width="80%" alt="">
            <div class="title">DAC 2024</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/2021.jpg" height="80%" width="80%" alt="">
            <div class="title">Graduates in 2021</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/2024_graduate/2024-1.jpeg" height="80%" width="80%" alt="">
            <div class="title">Graduation Party 2024</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/2025_graduate/1.jpeg" height="80%" width="80%" alt="">
            <div class="title">Graduation Party 2025</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/2025_graduate/4.jpeg" height="80%" width="80%" alt="">
            <div class="title">Graduates in 2025</div>
        </div>
        <div class="dotdiv">
            <span class="dot active"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
        </div>
        <div id="arrow">
            <img src="/assets/img/left.png" alt="" width="60" onClick="picplay(false)">
            <img src="/assets/img/right.png" width="60" alt="" align="right" onClick="picplay(true)">
        </div>
    </div>

</body>

<script>
    var imgIndex = 0;
    var imgDivArr = document.getElementsByClassName("imgdiv");
    var dotArr = document.getElementsByClassName("dot");
    /**
     *  播放图片
     *  参数r：是否正放，若为true，正放。若为false，倒放
     */
    function picplay(r) {
        for (let i = 0; i < imgDivArr.length; i++) {
            imgDivArr[i].style.display = "none";
            dotArr[i].className = "dot";
        }
        if (r) {
            imgIndex++;
            imgIndex = (imgIndex >= imgDivArr.length) ? 0 : imgIndex;
        } else {
            imgIndex--;
            imgIndex = (imgIndex < 0) ? imgDivArr.length - 1 : imgIndex;
        }
        imgDivArr[imgIndex].style.display = "block";
        dotArr[imgIndex].className = "dot active";
    }
    setInterval(picplay, 6000, true);

</script>





#### **News**
- Our paper "ICON-NIV: A Generalized Method for Mitigating the Impacts of IR Drop and Nonlinear I-V Effect in eNVM-based Accelerators" is accepted by DATE 2025. Congratulations to Jinpeng Liu.
- Our paper "RBC: A Randomness-Resistant Block-Grained Compaction" is accepted by DATE 2025. Congratulations to Tianqi Zhan.
- Our paper "MPFS: A Scalable User-Space Persistent Memory File System for Multiple Processes" is accepted by DATE 2025. Congratulations to Bo Ding.
- Our paper "CMD: A Cache-Assisted GPU Memory Deduplication Architecture" is accepted by TCAD 2025. Congratulations to Wei Zhao.
- Our paper "An Efficient Independent Read Scheme for Contemporary QLC SSDs" is accepted by TCAD 2025. Congratulations to Dong Huang.
- Our paper "SEED: Speculative Security Metadata Updates for Low-Latency Secure Memory" is accepted by TACO 2024. Congratulations to Xueliang Wei.
- Our paper "SAQO: Empowering Computational Storage Device for Efficient SQL Query Acceleration" is accepted by NAS 2024. Congratulations to Yao Deng.
- Our paper "COVER: Alleviating Crash-Consistency Error Amplification in Secure Persistent Memory Systems" is accepted by TACO 2024. Congratulations to Xueliang Wei.
- Our paper "FADESIM: Enable Fast and Accurate Design Exploration for Memristive Accelerators Considering Non-idealities" is accepted by TCAD 2024. Congratulations to Bing Wu.
- Our paper "DRCTL: A Disorder-Resistant Computation Translation Layer Enhancing the Lifetime and Performance of Memristive CIM Architecture" is accepted by MICRO 2024. Congratulations to Heng Zhou.
- Our paper "LpaqHP: A High-Performance FPGA Accelerator for LPAQ Compression" is accepted by ICPP 2024. Congratulations to Weilin Zhu.
- Our paper "Enabling Reliable Memory-Mapped I/O with Auto-snapshot for Persistent Memory Systems" is accepted by TC 2024. Congratulations to Bo Ding.
- Our paper "STAGGER: Enabling All-in-One Subarray Sensing for Efficient Module-level Processing in Open-Bitline ReRAM" is accepted by DAC 2024. Congratulations to Chengning Wang.
- Our paper "A Read Latency Variation Aware Independent Read Scheme for QLC SSDs" is accepted by DATE 2024. Congratulations to Dong Huang.

**We are looking for motivated undergraduates and master students to join the team, please feel free to contact me. (Email: tongwei@hust.edu.cn)**