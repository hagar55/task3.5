select Name from Students as s
join Friends as f 
on s.ID = f.ID
join Packages as p
on p.ID = s.ID
join Packages as fp
on fp.ID = f.Friend_ID
where p.Salary < fp.Salary
order by fp.Salary;
