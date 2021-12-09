| Field               | Type         |
| :------------------ | :----------- |
| ukprn               | varchar(8)   |
| institution         | varchar(100) |
| subject             | varchar(60)  |
| level               | varchar(50)  |
| question            | varchar(10)  |
| A_STRONGLY_DISAGREE | int(11)      |
| A_DISAGREE          | int(11)      |
| A_NEUTRAL           | int(11)      |
| A_AGREE             | int(11)      |
| A_STRONGLY_AGREE    | int(11)      |
| A_NA                | int(11)      |
| CI_MIN              | int(11)      |
| score               | int(11)      |
| CI_MAX              | int(11)      |
| response            | int(11)      |
| sample              | int(11)      |
| aggregate           | char(1)      |

nss表

向成千上万的英国高等教育毕业生。该调查问了22个问题，学生可以用“非常不同意”、“不同意”、“中性”、“同意”或“非常同意”来回答。这些列中的值代表回答该问题的学生总数的百分比。

## 1.Check out one row

**列出例子中`非常同意`的比例。**

### Correct answer

| A_STRONGLY_AG.. |
| --------------- |
| 23              |

## 2.Calculate how many agree or strongly agree

**列出`institution`和`subject`，`score`至少有100，问题为15。**

### Correct answer

| institution                                                  | subject                                   |
| ------------------------------------------------------------ | ----------------------------------------- |
| Kingston College                                             | (I) Education                             |
| Royal Holloway, University of London                         | (L) Geographical Studies                  |
| Solihull College                                             | (I) Education                             |
| Stafford College                                             | (D) Business and Administrative studies   |
| University of Southampton                                    | (E) Mass Communications and Documentation |
| University of Wolverhampton                                  | (7) Mathematical Sciences                 |
| University of Leicester                                      | (2) Subjects allied to Medicine           |
| University of Newcastle upon Tyne                            | (E) Mass Communications and Documentation |
| Bishop Grosseteste University College, Lincoln               | (F) Languages                             |
| University of Dundee                                         | (L) Geographical Studies                  |
| Universities of East Anglia and Essex; Joint Provision at University Campus Suffolk | (G) Historical and Philosophical studies  |

## 3.Unhappy Computer Students

**列出`institution`和`subject`，`score`低于50，问题为15，`subject`为'(8) Computer Science'。**

### Correct answer

| institution                                                  | score |
| ------------------------------------------------------------ | ----- |
| Blackburn College                                            | 45    |
| North Lindsey College                                        | 30    |
| Plymouth College of Art                                      | 47    |
| Somerset College of Arts and Technology                      | 48    |
| University of Wales, Newport                                 | 30    |
| Universities of East Anglia and Essex; Joint Provision at University Campus Suffolk | 45    |

## 4.More Computing or Creative Students?

**列出`subject`和回答总人数，问题为22，subject为'(8) Computer Science'和'(H) Creative Arts and Design'。**

### Correct answer

| subject                      | sum(response) |
| ---------------------------- | ------------- |
| (8) Computer Science         | 10612         |
| (H) Creative Arts and Design | 34370         |

