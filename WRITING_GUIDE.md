# THESIS WRITING GUIDE
## International University VNU-HCM -- CS/SE Undergraduate Thesis

> Huong dan nay duoc viet bang tieng Anh khong dau.
> Doc ky truoc khi bat dau viet.

---

## PHAN 1: QUY TRINH KIEM TRA TREN OVERLEAF

### Upload len Overleaf:
1. Zip toan bo thu muc `thesis_template/` thanh file `thesis_template.zip`
2. Vao overleaf.com -> New Project -> Upload Project
3. Upload file zip
4. Overleaf se tu detect `main.tex` la file chinh
5. Bam Recompile

### Loi thuong gap khi compile:
- **Missing image**: Xoa hoac comment dong `\includegraphics` neu chua co anh
- **Bibliography empty**: Sau khi them bib entries, bam Recompile 2 lan
- **Font error**: Dam bao dung `\usepackage[utf8]{inputenc}`

---

## PHAN 2: CACH TU DUY KHI VIET LUAN VAN

### Tu duy sai vs dung:

| SAI | DUNG |
|-----|------|
| "Toi se giai thich ky thuat X" | "Ky thuat X giai quyet van de Y vi..." |
| Viet nhu huong dan su dung | Viet nhu giai thich cho dong nghiep |
| Liet ke cac buoc da lam | Giai thich quyet dinh da chon |
| "Results are good" | "System achieves X% vs baseline Y%" |

### Cau hoi nen tu hoi truoc moi doan:
1. **Cau nay noi gi moi?** (Neu khong co gi moi, xoa di)
2. **Nguoi doc co the hoi "So sao?" khong?** (Neu co, viet them)
3. **Co so lieu, vi du cu the khong?** (Neu khong, them vao)

---

## PHAN 3: CAC CAU TRUC CAU HAY DUNG

### Mo dau section/chapter:
```
"This chapter presents / describes / reports..."
"[Component X] is responsible for [task] in the pipeline."
"Building on the design in Chapter 3, this chapter..."
```

### Gioi thieu quyet dinh thiet ke:
```
"[Approach A] was chosen over [Approach B] because..."
"This design decision was motivated by [reason]."
"An early version used [X]; it was replaced by [Y] because..."
"[Component] was initially designed to [A], but testing
 revealed [problem], leading to [change]."
```

### Trich dan tai lieu:
```
"\citet{smith2023} proposed [method], which [does what]."
"Prior work~\cite{jones2022} showed that [finding]."
"Unlike [approach in cite{x}], our system [difference]."
"To the best of our knowledge, no prior work has [gap]."
```

### Trinh bay ket qua:
```
"Table X shows that [system] achieves [X%] accuracy on [Y]."
"[Category A] queries are handled most reliably ([X%]),
 while [Category B] remains the weakest ([Y%])."
"The full system outperforms the baseline by [X] percentage
 points, with the largest gain on [category]."
```

### Phan tich ket qua (observe -> explain -> imply):
```
"[Statistic observed]. This is because [mechanism/reason].
 [Implication for design or future work]."
```

### Neu han che (honest + constructive):
```
"The system's handling of [X] is limited because [reason].
 In practice, this means [concrete consequence]. A possible
 fix would be [approach], though [challenge/trade-off]."
```

### Ket thuc doan / section:
```
"This [component/finding] is discussed further in
 Section~\ref{sec:X}."
"Chapter 4 builds on this design and describes its
 implementation."
"The implications of this result are examined in
 Section~\ref{sec:discussion}."
```

---

## PHAN 4: CHECKLIST TRUOC KHI NOP

### Tong the:
- [ ] Abstract: co du 5 phan (context, gap, objective, method, result)
- [ ] Moi chapter bat dau bang doan mo ta cau truc
- [ ] Moi section ket thuc co bridge sang section/chapter tiep
- [ ] Chapter 6 doi chieu tung objective voi ket qua cu the

### Ky thuat:
- [ ] Moi figure co caption ro rang, duoc \label va \ref
- [ ] Moi table co caption (phia tren), duoc \label va \ref
- [ ] Moi equation duoc danh so va giai thich ky hieu
- [ ] Moi viet tat duoc giai thich lan dau xuat hien

### Bibliography:
- [ ] Moi nguon trong .bib co it nhat 1 lan \cite{} trong van ban
- [ ] Khong co nguon trong van ban ma thieu trong .bib
- [ ] Tat ca cac \cite{} tro den dung entry trong bibliography.bib

### Ngon ngu:
- [ ] Khong co cau qua dai (>3 dong) ma khong dung dau phay
- [ ] Khong co doan qua ngan (chi 1 cau) -- nen co it nhat 3 cau/doan
- [ ] Spell-check chay xong (trong Overleaf: Edit -> Spell Check)

---

## PHAN 5: SO DO XEM CHAPTER NAO LIEN QUAN CHAPTER NAO

```
Chapter 1: Introduction
  |
  +-- Motivates ---> Chapter 2: Related Work
  |                    (background & literature)
  |
  +-- Defines ---> Chapter 3: Methodology
  |  (objectives)      (design & theory)
  |                       |
  |                       v
  |                  Chapter 4: Implementation
  |                    (how it was built & eval setup)
  |                       |
  |                       v
  |                  Chapter 5: Results & Discussion
  |                    (numbers + analysis)
  |                       |
  +-- Revisited -----> Chapter 6: Conclusion
     (objectives          (summary + future work)
      checked again)
```

Moi chapter phai lien ket ro rang voi chapter truoc va sau.
Neu mot chapter co the bi xoa ma khong anh huong den cac chapter
khac, co the no dang qua doc lap.

