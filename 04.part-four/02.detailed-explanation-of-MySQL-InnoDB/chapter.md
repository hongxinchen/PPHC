---
menu: MySQL InnoDB 详解
title: MySQL InnoDB 存储引擎详解
taxonomy:
    category: docs
chapterNumber: 8
---

在前几章中，我们通常以架构为武器，对性能问题进行降维打击。然而，本章不同，我们要啃硬骨头：深入理解 MySQL 的 InnoDB 存储引擎，以便读者们能够顺利阅读下一章。

#### 还记得我们的目标吗？一百万 QPS

在经过性能优化的电商业务中，假设每次 API 调用平均执行五条 SQL，那么数据库的 QPS 就是 500 万。稍微接触过一些高并发系统的人都能一眼看出，这是一个多么惊人的数字。对于开源 MySQL 来说，单机一万的 QPS 已经非常优秀，而 500 万简直就像天方夜谭。别着急，慢慢往后看，这真的有可能实现。