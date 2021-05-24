use bd_security;

-- insert users
insert into users(username,password,nombre,apellidos,email,celular,state)
values('antonie','a123','Antonie','Huertas saint','antonie@hotmail.com',99787567,'ACTIVE');

insert into users(username,password,nombre,apellidos,email,celular,state)
values('werther','w123','Wherther','Bravo Valdez','wherther@gmail.com',9766666789,'ACTIVE');

insert into users(username,password,nombre,apellidos,email,celular,state)
values('margarita','m123','Margarita','Guevara Ñahui','margarita@gmail.com',988736855,'ACTIVE');

insert into users(username,password,nombre,apellidos,email,celular,state)
values('charlotte','c123','Charlotte','Toro Díaz','charlotte@gmail.com',999444333,'ACTIVE');

-- Update
update users set password='$2a$10$3be/svOnjJMcC97Qi30AveA9Ki9vvrZdgK/gkHusMZkkoUzP9zyF.' where user_id=1;
update users set password='$2a$10$VMVoktOjAtSB5gxV9jE.WOMwG00auqgacdoyZ18H27B/Yicn2yzWa' where user_id=2;
update users set password='$2a$10$DpChF1kAt2B4eamEeemoquKcMMM8MJQkXQnkU3IKyzphL1WYoG9QK' where user_id=3;
update users set password='$2a$10$S7NqgyAYAFS4AwlV9L15neMpvwDDiNgLBDnpcqKTaXAAcZm5gOs.m' where user_id=4;


-- insert roles
insert into roles(type) values('USER');
insert into roles(type) values('ADMIN');
insert into roles(type) values('DBA');

-- insert users-roles
insert into users_roles(user_id,role_id) 
select user_id, role_id from users u, roles r where u.username='antoine' and r.type='USER';

insert into users_roles(user_id,role_id)
select user_id, role_id from users u, roles r where u.username='werther' and r.type='USER';

insert into users_roles(user_id,role_id)  
select user_id, role_id from users u, roles r where u.username='margarita' and r.type='ADMIN';

insert into users_roles(user_id,role_id)  
select user_id, role_id from users u, roles r where u.username='charlotte' and r.type='ADMIN';

insert into users_roles(user_id,role_id) 
select user_id, role_id from users u, roles r where u.username='charlotte' and r.type='DBA';

-- data
select * from users order by user_id;
select * from roles order by role_id;
select * from users_roles order by user_id,role_id;

