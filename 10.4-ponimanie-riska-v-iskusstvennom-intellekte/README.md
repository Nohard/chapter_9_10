# 10.4 Понимание риска в искусственном интеллекте

Одна тема, о которой я часто говорю на конференциях и в печати, это риск искусственного интеллекта с точки зрения доверия и контроля. Я говорю здесь не о каком-то вышедшем из-под контроля искусственном интеллекте, а скорее о том, является ли ИИ надежным.

Довольно интересно, что ИИ, которым мы занимались, - в частности, искусственные нейронные сети, - делает то, что мало какие компьютерные программы могут сделать.

Получая те же самые входные данные и условия, выходные данные системы ИИ не всегда одни и те же. При одинаковых входных данных ИИ иногда будет давать другой ответ.

Формальное название такого поведения - недетерминизм.

Есть второе следствие из этого. Получая те же входные данные, процесс ИИ иногда будет занимать разное время выполнения своей задачи.

Это просто не нормальное поведение для компьютера. Мы привыкли к 2 + 2 = 4 на довольно консистентной основе от компьютера. На самом деле, мы зависим от этого. Помните, что компьютеры управляют вашими авиалайнерами, сохраняют вас в живых в больнице, отправляют астронавтов на Луну. Как мы можем иметь дело с компьютером, иногда говорящим 2 + 2 = 2, и занимающим разное количество времени, чтобы сделать это?

Вы можете убедиться в этом сами - посмотрите на примеры, когда мы тренировались на нейронных сетях. Достигли ли мы когда-либо 100% успеха в тренировочном заезде, где мы получили все правильные ответы? Нет, ни разу.

Это потому, что искусственные нейронные сети являются универсальными аппроксимационными функциями, которые сопоставляют входные данные - которые могут быть довольно сложными – с выходными. Они делают это, имея дело с вероятностями и средними величинами, которые развивались с течением времени. Вы можете считать искусственный нейрон вероятностным движком, который говорит, что _45 из последних 50 раз, когда я получил этот набор входных данных, результат должен был быть истиной. Вероятнее всего, это будет истиной в этот раз_. И он устанавливает себя истинным. У нас могут быть миллионы маленьких искусственных нейронов в нашей сети, каждый из которых будет производить один и тот же расчёт. В результате получается очень обоснованное предположение об ответе.

Для большинства приложений наших нейронных сетей это приемлемое поведение. Мы классифицируем фотографии, и это приемлемо, если несколько будет неправильных. Мы делаем в Google поиск утконоса \(platypus\), и получаем одно изображение из 100, на котором теннисные кроссовки Platypus. Это приемлемо для поиска в Google, но что, если бы мы делали что-то более серьезное, - например, распознавали пешеходов в беспилотном автомобиле. Было бы приемлемо, если бы мы неправильно распознали одного пешехода из 100 и не объехали его? Конечно же нет. Вот почему сейчас мы не допускаем систему ИИ выполнять такие важные задачи. Но люди хотят использовать ИИ таким образом - на самом деле, очень сильно. Было бы здорово иметь ИИ, которой бы распознавал гусей в полете и говорил бы авиалайнеру, как их избежать. Было бы здорово, если бы ИИ распознавал, что пациент был неправильно диагностирован в больнице и нуждается в немедленном внимании. Но мы не сможем сделать это до тех пор, пока не придумаем процессы управления недетерминированной и, следовательно, ненадежной природой ИИ.

Теперь, в наши дни, мы постоянно имеем дело с недетерминированными элементами в автомобилях. Они называются водителями. Мы также знаем, что 94% автомобильных аварий \(5\) вызваны этим человеческим элементом за рулем, поэтому мы и нуждаемся в беспилотных автомобилях с лучшим процентом. Как мы справляемся с человеческими водителями? Мы требуем, чтобы они были определенного возраста, а это значит, что они приобрели опыт. Они должны пройти тест, демонстрирующий компетентность в выполнении задач. Они должны продемонстрировать согласие с правилами и нормативно-правовыми актами путем сдачи теста на знание. И они должны периодически проходить повторную сертификацию, обновляя свои лицензии. Мы также требуем ремни безопасности и подушки безопасности, чтобы частично смягчить риск ошибки человеческого водителя, путём частичного уменьшения получаемой травмы.

Мы можем применить эти типы критериев к ИИ. Мы можем требовать определенное количество случаев обучения. Мы можем проверять и демонстрировать уровень компетентности. Мы можем заранее предсказывать уровень погрешностей или ошибок, и принимать меры для снижения этого риска. Возможно, мы можем иметь две системы искусственного интеллекта, одна из которых обнаруживает препятствия, а другая обучена распознавать ошибки первой. Если у нас есть 90% шанс того, что первый ИИ будет прав, и еще 90%, что второй ИИ будет прав, тогда у нас есть шанс 90% + \(90% из 10%\) = 99% избегания ошибки.

Я думаю, что ключом к использованию ИИ в критических для безопасности приложениях является возможность прогнозировать риск заранее, и заранее разрабатывать ИИ так, чтобы смягчить либо причину риска, либо его следствие.

