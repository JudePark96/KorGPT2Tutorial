# KorGPT2Tutorial
Tutorial for pretraining and finetuning Korean GPT-2 model

Sample model download: https://drive.google.com/drive/folders/124Uux07pym2YaCeQKQWNhzhLNeIlLm7r?usp=sharing   
(100,000 sentences, 1 epoch)   

## 0. Setup
### Virtual Env (Optional)
```bash
python3 -m venv .venv
source .venv/bin/activate
```
### Install packages
```bash
pip install -r requirements.txt
```


## 1. Make vocab and tokenizer from corpus
```python make_tokenizer.py```

## 2. GPT-2 training from scratch   
if you want to train GPT-2 from existing model, add the argument '--init_model'   
```python pretrain_gpt2.py --do_train --do_eval --eval_data_file=pretrain_data/datas/sample_text.txt --model_type=gpt2 --train_data_file=pretrain_data/total_pretrain_data.txt --num_train_epochs=1```   

## 3. Text generation test
```python generation_text.py```

input: 이순신은 조선
-  이순신은 조선 시대 이순신은 무솔한 이순신의 모습을 생생하게 재현했다.
 이순신은 일제강점기 조선의 한 축을 책임지고 있다.
 임진왜란 당시 이순신은 무솔한 이순신을 살려내 이순신의 모습을 담은 전시회를 가졌다.
 이순신은 '역사'로서 이순신을 대표하는 이순신답게, 이순신은 일제강점기 조선 조선 조선 시대의 대표적인 작품 중 하나다.
 이순신은 조선의 역사와 전통을 담아내기 위해 선조들의 관심을 끌었고, 조선 시대 조선총독부에서 이순신이 보여준 이순신의 모습은 이순신과 이순신을 가장 가까이에서 볼 수 있는 대목이다.
 이순신은 1900년 전란 중인 조선총독부 경무국과 조선군사정관을 지냈다.
 이순신은 일제강점기 조선의 역사를 한 획을 그었다.
 이순신 시대 이순신은 조선총독부 경무국장으로 근무했다.
 그 동안 이순신은 조선총독부 경무국과 조선군의 역사를 다년간 지냈다.
 그 동안 이순신의 업적을 재현하기 위해 이순신의 발자취를


input: 밤하늘의 별
-  밤하늘의 별과 비슷한 것인데도 불구하고 하늘엔 태양이나 어두운 기운이 스며 있고, 눈이 하늘보다 높지만 그마저도 태양이나 어두운 색이었다. 빛의 별이나 태양의 별과 마찬가지로 하늘보다 훨씬 높고 밝은 별이 더 많았을 것이다. 하늘엔 태양이나 어두운 기운이 가득 고여 있고, 하늘이 더 밝게 빛났으며, 이 별을 관측하는 것도 하늘의 별과 같은 것이라고 생각했다. 그 별들은 태양을 처럼, 밝은 별들이 더 밝게 빛났었다. 그 별이 빛난 별과 달리 태양이 빛난 별이 더 더 밝게 빛났기 때문이다. 별의 별들은 하늘의 별과 별에 대해 별과 별 사이의 차이점을 구분하였다.


## 4. lyric finetuning and generation
Full data is not availabled but you can download sample model from Google drive link above   
```python lyric_finetuning.py```   
```python lyric_generation.py```   

input: 봄바람이 휘날리며
- 봄바람이 휘날리며//살며시 내게 속삭일 때 난 고백하지 못해//그대 날 보는 내 마음을//설레였던 그대 미소 속에 나를 녹여//달나라 그대와 마주앉아//함께한 꿈들 그대 꿈속에서도//함께해 우리 함께한//그 꿈을 찾아//그대라는걸 그대만이 알죠//사랑해요 그대가 그댄 나의 사랑을//늘 달 한 순간도 변함없죠//내 손을 잡던 따뜻한 바람에도//그대가 내 곁을 지켜줄 사람//내 곁을 지켜줄 사람//사랑합니다//그대와 그대 그대 그대 그대죠//그대여야만 하는 시간//그대를 기다리는 이 맘//늘 달 한 순간도 변함없죠//내 곁을 지켜줄 사람//사랑합니다//그대와 그대 그대죠//그대여야만 하는 시간//그대를 기다리는 이 맘//늘 달 한 순간도 변함없죠//내 곁을 지켜줄 사람//사랑합니다//그대와 그대죠//그대여야만 하는 시간//그대를 기다리는 이 맘//늘 달 한 순간도 변함없죠//내 곁을 지켜줄 사람//사랑합니다//그대와 그대죠//그대여야만 하는 시간//그대를 기다리는 이 맘
 
 
input: 비 내리는 등대에서
- 비 내리는 등대에서 내리면// 그 곳으로 날아가요// 나를 향해 가는 노래// 나의 노래// 내 노래를 부르죠// 널 사랑해 사랑해줘// 언제나 내 곁에서 함께 웃어요// 모든 걸 알아줄래요// 우리 함께 하는 이 노래를// 매일 나와 함께 할 그대// 언제나 내 곁에서 함께 할 그대// 언제나 내 곁에서 함께 웃을 그 사람// 언제나 내 곁에서 함께 웃어요// 모든걸 알아줄래요// 우리 함께 하는 이 노래를// 매일 나와 함께 할 그대// 언제나 내 곁에서 함께 웃어요// 모든 걸 알아줄래요// 우리 함께 하는 이 노래를// 매일 나와 함께 할 그대// 언제나 내 곁에서 함께 웃어요// 모든걸 알아줄래요// 우리 함께 하는 이 노래를// 늘 내 곁에서 함께 웃어요// 모든걸 알아줄래요// 우리 함께 하는 이 노래를// 매일 나와 함께 할 그대
 
 
input: 좁고 좁은 저 문으로
- 좁고 좁은 저 문으로// 나를 둘러 싼// 날들은 매일 밤 새침 없이 문을 두드리네// 날 위한 이 밤// 아무도 모르게 날 밝혀주네// 우리 둘만 있어// 나의 작은 방 안에 가득// 가득// 너의 문을 두드리네// 나를 본 이 사람// 내 마음을 들뜨게 하네// 아무도 모르게 날 밝혀주네// 날 바라보는 날 지켜준// 널 사랑하는 나// 모든 게 너의 달과 같아// 네가 있어 내 곁에 있어// 너의 마음을 들뜨게 하네// 아무도 모르게 날 밝혀주네// 날 바라보는 날 지켜준 나// 모든 게 너의 달과 같아// 네가 있어 내 곁에 있어// 너의 마음을 들뜨게 하네// 아무도 모르게 날 밝혀주네// 날 바라보는 날 지켜준 나// 모든 게 너의 달과 같아// 네가 있어 내 곁에 있어// 너의 마음을 들뜨게 하네// 아무도 모르게 날 밝혀주네// 날 바라보는 날 지켜준 나// 모든 게 너의 달과 같아// 네가 있어 내 곁에 있어// 너의 마음을 들뜨게 하네// 아무도 모르게 날 밝혀주네// 날 바라보는 날 지켜준 나// 모든 게 너의 달과 같아// 네가 있어 내 곁에 있어

 
## 5. Paraphrasing finetuning
- https://github.com/MrBananaHuman/KoGPT2ForParaphrasing









