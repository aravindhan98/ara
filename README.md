public class applicationuser:identityuser
{
public class applicationDbcontext:identityDBcontext<applicationuser>
  {
  private static bool _created;
  
  public applicationDbcontext()
  {
  if(!_created)
  {
      databse.asrelation().applymigrations();
      _created=true;
      }
      }
