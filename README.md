# Pgadmin4-6.ODEV
6.ÖDEV
--1.)film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

select round(avg(rental_rate),3) from film

--2.)film tablosunda bulunan filmlerden kaçtanesi 'C' karekteri ile başlar?

select count(title) from film
where title like 'C%'

--3.)ilm tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

select max(length) from film
where rental_rate=0.99

--4.)ilm tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

select count(distinct(replacement_cost)) from film
where length>150
