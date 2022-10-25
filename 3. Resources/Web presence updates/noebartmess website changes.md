# noebartmess website changes


Changes to theme

~Change font color from yellow to blue~
Add to child theme css: 

a {
	color:#0066bf;
	text-decoration:underline;
}

~Underline current page title~
Add to child theme css: 

.current_page_item{
	text-decoration: underline;	
} 

~Get blog page to say "Blog"~

In the theme file's index.php file (which needs to be the parent theme, Responsive Blogily, not Fluid Basics or the child I made: add, just after the H1 that has the screen-reader-text class (note: had to go through Bluehost cpanel file manager): 			
<h1 class="blog-page-title"><?php single_post_title(); ?></h1>

And added to my child css file via theme editor: 

.blog-page-title {
	text-indent: 25px;
}

~Left-justify page titles~

Add to my child css file: 
h1.entry-title, h2.entry-title, h2.entry-title a:hover, h2.entry-title a:active {
	font-family: 'Quicksand';
	font-weight:normal;
	color: #000;
	font-size: 30px;
	text-align: left; 
	line-height: 150%;
	margin-top: 0px;
}

~Reduce spacing on posts page between title and body~
Note: the spacing is there because the meta info is not showing.

IN my child css file add: 

.blog-entry-meta {
	font-size: 5px;
		margin-bottom: 10px;
}

~Change post title on posts page to h3 size to match h3~

In my child css file add:
.single-blog-entry-title {
	font-size: 20px;
	margin-bottom: 0px;
}


====
Page bio

Noe (rhymes with Zoe) writes humorous science fiction and fantasy as well as nonfiction on representation of autistic characters in fiction. She's also edited a nonfiction anthology with contributions by adult-diagnosed autistic people. 

Noe is a graduate of the 2016 Clarion West Writers Workshop. You can find her on Twitter at @noebartmess. Contact info: noe.bartmess@gmail.com or use the contact form. 

#z-archives
