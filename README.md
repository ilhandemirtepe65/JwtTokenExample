# JwtTokenExample
 * Redis ne zaman ve nasıl kullanılmalıdır
   * eğer data az değişirse,yani sürekli güncelenen bir data değilse redis kullanabilirsiniz.
   * GetAll için için :İlk başta redise bak eğer data varsa redisten oku,eğer yoksa db den oku.Dbden okuduğun Redisle set et,hemde ekranda göster
   * GetById için :Redise bak,eğer ilgili data rediste varsa redisten oku ,yoksa dbden getir
   * Delete,Update,Insert de -->Şunu izle
            await _context.SaveChangesAsync();
            _cacheService.RemoveData("Product");
   
               
