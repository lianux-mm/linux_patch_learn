# linux_patch_learn

patch review and learn

## THP

- 2010-11-03 [\[PATCH 00 of 66\] Transparent Hugepage Support #32 - Andrea Arcangeli](https://lore.kernel.org/all/patchbomb.1288798055@v2.random/)
  - 支持 anon THP
  - v33 https://lore.kernel.org/all/20101215051540.GP5638@random.random/
- November 11, 2014 [Transparent huge page reference counting \[LWN.net\]](https://lwn.net/Articles/619738/)
- 2015-10-06 [\[PATCHv12 00/37\] THP refcounting redesign - Kirill A. Shutemov](https://lore.kernel.org/linux-mm/1444145044-72349-1-git-send-email-kirill.shutemov@linux.intel.com/)
  - 新的 refcount mapcout 方案
  - 支持 THP 的 PMD map 和 PTE map 共存
- 2016-03-07 [\[PATCHv2 0/4\] thp: simplify freeze_page() and unfreeze_page() - Kirill A. Shutemov](https://lore.kernel.org/linux-mm/1457351838-114702-1-git-send-email-kirill.shutemov@linux.intel.com/)
  - 一个比较小的 patch set，在 split huge page 时，使用通用的 rmap walker `try_to_unmap()`，简化了 `freeze_page()` 和 `unfreeze_page()`。
- 2016-05-11 [Transparent huge pages in the page cache \[LWN.net\]](https://lwn.net/Articles/686690/)
- 2016-06-15 [\[PATCHv9-rebased2 00/37\] THP-enabled tmpfs/shmem using compound pages - Kirill A. Shutemov](https://lore.kernel.org/linux-mm/1466021202-61880-1-git-send-email-kirill.shutemov@linux.intel.com/)
  - 支持 tmpfs/shmem THP
- 2022-11-03 [\[PATCH 0/3\] mm,huge,rmap: unify and speed up compound mapcounts - Hugh Dickins](https://lore.kernel.org/linux-mm/5f52de70-975-e94f-f141-543765736181@google.com/)
  - 优化 compound mapcount
- 2024-05-21 [Facing down mapcount madness \[LWN.net\]](https://lwn.net/Articles/974223/)
- 2024-02-26 [\[PATCH v5 0/8\] Split a folio to any lower order folios - Zi Yan](https://lore.kernel.org/linux-mm/20240226205534.1603748-1-zi.yan@sent.com/)
  - 支持将 folio split 到任意 low order
- 2025-03-07 [\[PATCH v10 0/8\] Buddy allocator like (or non-uniform) folio split - Zi Yan](https://lore.kernel.org/linux-mm/20250307174001.242794-1-ziy@nvidia.com/)
  - 支持 non-uniform folio split
- 2025-05-12 [\[PATCH v2 0/8\] ext4: enable large folio for regular files - Zhang Yi](https://lore.kernel.org/all/20250512063319.3539411-1-yi.zhang@huaweicloud.com/)
  - 为 ext4 regular files 支持 large folio

## mTHP

- 2025-08-19 [\[PATCH v10 00/13\] khugepaged: mTHP support - Nico Pache](https://lore.kernel.org/linux-mm/20250819134205.622806-1-npache@redhat.com/)
- 2025-08-20 [\[RFC PATCH 00/11\] add shmem mTHP collapse support - Baolin Wang](https://lore.kernel.org/linux-mm/cover.1755677674.git.baolin.wang@linux.alibaba.com/)

selftests

- 2025-08-18 [\[PATCH v5 0/5\] Better split_huge_page_test result check - Zi Yan](https://lore.kernel.org/linux-mm/20250818184622.1521620-1-ziy@nvidia.com/)

## rmap

selftests

- 2025-08-19 [\[Patch v4 0/2\] test that rmap behaves as expected - Wei Yang](https://lore.kernel.org/all/20250819080047.10063-1-richard.weiyang@gmail.com/)

## madvise

- 2025-06-07 [\[PATCH v4\] mm: use per_vma lock for MADV_DONTNEED - Barry Song](https://lore.kernel.org/all/20250607220150.2980-1-21cnbao@gmail.com/)

## msharefs

- 2025-08-20 [\[PATCH v3 00/22\] Add support for shared PTEs across processes - Anthony Yznaga](https://lore.kernel.org/linux-mm/20250820010415.699353-1-anthony.yznaga@oracle.com/)
