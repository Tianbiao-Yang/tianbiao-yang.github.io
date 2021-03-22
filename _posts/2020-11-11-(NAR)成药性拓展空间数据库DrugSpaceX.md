---
layout:     post                 # 使用的布局（不需要改）
title:      DrugSpaceX            # 标题 
subtitle:   成药性拓展空间数据库DrugSpaceX
date:       2020-11-11              # 时间
author:     Yichen Yang                      # 作者
header-img: img/post-bg-dreamer.jpg  #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - Paper
---
# 成药性拓展空间数据库DrugSpaceX


    在创新药物研发中，一个核心问题是如何快速发现具有理想生物学特性的新化学实体。然而，满足Lipinski's类药性的化学空间所包含的理论分子数可能超过1063【1】，如何更高效地探索这样巨大的多样性空间，找到具有良好的可合成性和成药性的新分子是摆在计算化学家和药物化学家面前的一道难题。针对这一问题，Reymond团队利用穷举法构建重原子数在13到17范围之内的分子结构，建立了包含有166亿个化合物的GDB库【2】；Levré等人从市售的炔烃和叠氮化物出发通过使用Click反应规则构建了Zinclick数据库【3】，该库具有较好的可合成性但结构类型相对单一；此外，也有一些基于人工智能(Artificial Intelligence，AI) 方法，例如Segler等人利用LSTM模型设计集中化合物库【4】，Zhavoronkov等人将基于生成对抗网络 (GANs)的AI技术应用到化学空间探索【5】。虽然方法众多，但这些虚拟化合物库都面临着多样性、可合成性和成药性的多方面问题。